# Issue Report: Mounting /dev/sdc3

## 1. Identify the Problem
I am attempting to mount `/dev/sdc3` to my `/etc/fstab` configuration on EndeavourOS using the `ntfs3` driver because I heard it offers better compatibility and performance. After running `sudo mount -a`, I encounter an error. The drive could not be mounted.

## 2. Establish a Theory of Cause
I hypothesise that the issue might be related to the permissions of the mount directory.

### Actions Taken:
- I check the mount directory and see that it is owned by `root` only.

## 3. Test the Theory
I attempt to change the ownership of the mount directory to my user account (`maiks`) by running the following command:

`sudo chown maiks:maiks /path/to/mount/directory`
I verify the change by checking the directory’s ownership.

Using `ls -ld` I see that ownership of the directory is now correctly set to maiks.

## 4. Evaluate Results
I run `sudo mount -a` again to see if the issue persists.

The same error occurs.

I check the logs using `sudo dmesg | tail -n 20` as instructed in the error message.

The logs mention the error being a "dirty" NTFS partition that needs a `chkdsk` command from a Windows environment.

## 5. Establish a New Theory of Cause
I theorise that I don't have to boot a windows environment, and I can use a Linux alternative to `chkdsk`.

## 6. Test the Theory
I attempt to run `ntfsfix` to fix the partition without booting into Windows:

`sudo ntfsfix /dev/sdc3`

## 7. Evaluate Results
The error persists, and the logs still report the "dirty" partition issue.

## 8. Establish a New Theory of Cause
I hypothesise that the system may have already initialised another driver for /dev/sdc3.

Actions Taken:
I run sudo blkid /dev/sdc3 and find that the NTFS driver being used is ntfs-3g, not ntfs3.

## 9. Test the Theory
I reboot the device to see if booting with the new initialisation settings in /etc/fstab help.

## 10. Evaluate Results
The device does not boot, and I see the error related to the dirty partition again.

I immediately recognise two issues:

**First:** 
ntfs3 is for data integrity across windows and linux while simultaneously offering better performance, but that does not mean it's also better for my use case, because i just want to be able to access my old windows folders easily while on linux.

**Second:**
I forgot to add the nofail option to the /etc/fstab entry for the NTFS partition, which is why the system failed to boot instead of just failing to mount the partition.

## 11. Establish a Plan of Action
I will use ntfs-3g for /dev/sdc3 to avoid the dirty partition error and better handle the mount.

I will update /etc/fstab to add the nofail option to the /dev/sdc3 entry, so the system won't fail to boot if the partition is unavailable.

I will do only one at a time to isolate variables.

## 12. Implement Plan
Steps Taken:
I logged in as root when prompted by the terminal.

I edited the `/etc/fstab` file using `sudo nano /etc/fstab`.

I navigated to the final entry for `/dev/sdc3` and changed `ntfs3` to `ntfs-3g`.

I did not yet add nofail, as I wanted to test the change of the driver first.

I saved the changes and rebooted the system.

## 13. Verify Full System Functionality
Upon reboot, the system boots normally, and all drives are correctly mounted without issues.

Results:
The issue is resolved. Every partition now mounts correctly, and Linux boots as expected.

## 14. Document Findings
What Went Wrong: The initial error was caused by the default mount path not being accessible to my user profile. Where I went wrong in the troubleshooting process is I changed two variables at once, the NTFS driver and the ownership of the mount directory, before rebooting the system to properly assess the effects of each change. It took some troubleshooting to realise that the ntfs3 driver is not necessarily the best option for my use case, I also made the mistake of omitting the `nofail` flag on the relevant `/etc/fstab` entry, but this ended up only hastening my troubleshooting process.


How to Prevent: Going forward, I will use ntfs-3g for mounting old Windows clones that don't need booting, and use ntfs3 for mounting Windows partitions when data integrity across both OSes is key. I will also add the nofail option to /etc/fstab entries for non-essential drives, so they don’t block the boot process if they are unavailable.

## Notes:
NTFS3 vs. NTFS-3G: The ntfs3 driver is designed for data integrity between Windows and Linux and offers better performance, but it may not be suitable for all use cases. The ntfs-3g driver is more stable for general use.

nofail Option: Always use nofail for non-essential drives to prevent boot failures.

## Next Steps:
- Reformat my empty drives to not use NTFS
- Copy all important folders from old Windows install to a Linux friendly partition


