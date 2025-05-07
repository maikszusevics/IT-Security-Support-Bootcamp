# Issue Report: Non-root Drives Not Automatically Mounting on Linux Boot


## 1. Identify the Problem

When booting into my Linux system, only the root drive is automatically mounted.  
I want **all drives** mounted automatically at startup to avoid repeating the manual process of mounting through CLI after every reboot.


## 2. Establish a Theory of the Cause

Initial theory:

- Drives aren't listed in `/etc/fstab`, which is responsible for controlling filesystem mounts at boot.
- System relies on manual CLI mounting or mounting via desktop environment tools for removable media.


## 3. Test the Theory

**Check Current Mount Points**

Ran the following:

`lsblk -f`
![](lsblk.png)

This displayed the UUIDs, filesystem types, and mountpoints.


**Check `/etc/fstab`**

`cat /etc/fstab`
![](Learning/Personal-Troubleshooting-Knowledge-Base/Images/cat.png)

Only root and a few system partitions (like `/home`, `/var`, `/boot/efi`) were listed.


## 4. Evaluate Results: Theory Confirmed?

Confirmed: **None of the other data drives were present** in `/etc/fstab`.

Therefore, the system doesn’t know to mount them on boot.


## 5. Establish a Plan of Action

Plan:

- Use `lsblk -f` to gather UUIDs and filesystem types for all non-mounted drives.
- Create custom mount points under `/mnt/` or `/media/`.
- Add entries for each drive in `/etc/fstab` using UUIDs for stability.
	- Ensure stability when removable drives are missing.
	- Create a **backup** of the original `/etc/fstab` in case of misconfiguration.
- Test mounts manually first to validate syntax.
- Reboot and test.

## 6. Implement the Plan

### Step 1: Identify Drive Info

Ran:
`lsblk -f`

![](lsblk.png)
>/dev/sdc3 is only mounted on /mnt/windows because I've been manually mounting it when I need access to documents in my old documents folder

Collected UUIDs for the following partitions:

- `/dev/sda1`, `/dev/sdb1`, `/dev/sdd1`, `/dev/sde2`, `/dev/sdf1`, 

One of the drives listed (`/dev/sdf1`) is a **removable drive** that might not be present when booting, which might cause errors or delays when the system tries to mount it. To prevent this, the commands **`nofail`** and **`x-systemd.device-timeout=1s`** are used in the `/etc/fstab` entry:
`UUID=BC40B6C340B68424 /run/media/maiks/movie auto defaults,nofail,x-systemd.device-timeout=0s 0 0`

| Option                        | Purpose                                 |
| ----------------------------- | --------------------------------------- |
| `0 0` (last two columns)      | Skip dump and fsck                      |
| `nofail`                      | Avoid boot failure if device is missing |
| `x-systemd.device-timeout=0s` | Reduce boot delay if device is missing  |
### Step 2: Create Mount Points

Used the command:

`sudo mkdir -p /mnt/sda1 /mnt/sdb1 /mnt/sdd1 /mnt/sde2`

### Step 3: Backup fstab

Used the command:

`sudo cp /etc/fstab /etc/fstab.bak`



![](create.png)


### Step 4: Edit `/etc/fstab`

Opened with:

`sudo nano /etc/fstab`

![](nan.png)

Added entries:

```
UUID=C0404E01404DFEA2  /mnt/sda1  ntfs3  uid=1000,gid=1000,dmask=022,defaults,noatime,nofail  0 0  
UUID=4AB6AB3BB6AB2683  /mnt/sdb1  ntfs3  uid=1000,gid=1000,dmask=022,defaults,noatime,nofail  0 0  
UUID=B0BEA362BEA31FB8  /mnt/sdd1  ntfs3  uid=1000,gid=1000,dmask=022,defaults,noatime,nofail  0 0  
UUID=4E1052E61052D515  /mnt/sde2  ntfs3  uid=1000,gid=1000,dmask=022,defaults,noatime,nofail  0 0  
UUID=BC40B6C340B68424  /run/media/maiks/movie ntfs3    defaults,nofail,x-systemd.device-timeout=0s 0 0  
```
> These settings are safe for a **single-user system** because there's no risk of unauthorised access to files by other users, but for multi-user systems, you would need to consider stronger access control mechanisms, like restricting user/group access rules and read/write permissions. 

| **Option**                      | **Explanation**                                                                                                                                                                            |
| ------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **UUID**                        | A unique identifier for each partition, used to ensure that the correct drive is mounted even if the device name changes (e.g., `/dev/sda1` to `/dev/sdb1`).                               |
| **/mnt/sda1, /mnt/sdb1, etc.**  | The mount points where the drives will be accessible in the file system (e.g., `/mnt/sda1` is the location where the `sda1` drive will be mounted).                                        |
| **ntfs3**                       | The file system type. `ntfs3` is the driver that provides support for NTFS file systems in Linux, offering better compatibility and performance than older drivers.                        |
| **uid=1000**                    | Sets the user ID for ownership of the mounted file system. In this case, `1000` is typically the first user created on the system (your main user).                                        |
| **gid=1000**                    | Sets the group ID for ownership of the mounted file system. This ensures that the files are owned by the same user group as the user ID (`1000`), which is typically your main group.      |
| **dmask=022**                   | Sets the default permissions for directories. In this case, `022` means that directories will have `755` permissions, i.e., read/write/execute for the owner, and read/execute for others. |
| **defaults**                    | A shorthand for the default mount options. This includes read/write access, support for device files, and async operations.                                                                |
| **noatime**                     | Disables updating the "last access time" (`atime`) when a file is accessed. This improves performance by reducing unnecessary writes to the file system.                                   |
| **nofail**                      | Ensures that the system won't stop the boot process if the drive cannot be mounted (e.g., the drive isn't plugged in or is missing).                                                       |
| **x-systemd.device-timeout=0s** | This option sets the timeout for waiting for the device to be ready during boot. By setting it to `0s`, it tells the system to not wait at all if the device is not detected.              |
| **0 0**                         | For the last two entries, the `0 0` values indicate that these file systems won't be checked or dumped at boot. This is typical for external or removable drives.                          |



Used `cat` to confirm:


![](edited.png)

### Step 5: Test the Mounts Manually

`sudo mount -a`

![](hint.png)


![](work.png)


No errors were returned - confirmed mounts succeeded.

## 7. Verify Full System Functionality

- Rebooted the machine.
- All drives added to the `/etc/fstab` are mounted correctly on boot.

## 8. Document Findings

### What Went Wrong:

- Drives were not mounting because they weren’t specified in `/etc/fstab`.
- This led to repetitive manual mounting after every reboot.

### How to Mount Drives Automatically (Summary):

- Use `lsblk -f` to get UUIDs and filesystem types.
- Create persistent mount points in `/mnt/`.
- Add entries to `/etc/fstab` using UUIDs, e.g.:
    `UUID=xxxx-xxxx /mnt/sdX1 auto defaults,nofail 0 2`
	    - Consider what the drive is being used for - **If it stores sensitive data, add appropriate access control and permissions settings within the `fstab`**.
	    - Use `x-systemd.device-timeout=1s` to prevent long delays when booting without listed removable drives.
- Test mounts with `sudo mount -a` before reboot.
- Back up original `/etc/fstab` before editing.

### Preventative Measures:

- For every fresh Linux install, configure `/etc/fstab` early for all persistent storage.    
- Always use UUIDs to avoid device name changes (e.g., `/dev/sda` becoming `/dev/sdb` after a reboot).


## Notes

- /dev/sdc3 had issues with mounting beyond inclusion in /etc/fstab. This is documented in [another ticket.](/Learning/Personal-Troubleshooting-Knowledge-Base/Windows-clone-mounting-fix.md)