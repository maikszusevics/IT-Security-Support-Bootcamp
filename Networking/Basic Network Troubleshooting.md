# Intro

### Loopback Interface

The **loopback interface** is a special network interface used for testing the TCP/IP stack within a device. It is commonly tested with:

- `ping 127.0.0.1`

- `ping localhost`

This test ensures that the [TCP/IP](TCP-IP%20Stack.md) stack is functioning, as the request never leaves the system.


# Network Troubleshooting – Basic Ping Checks

1. **Ping Localhost**  
    `ping 127.0.0.1`  
    Checks if TCP/IP stack and NIC are functioning.
    
2. **Ping Own IP**  
    `ping [your_IP]`  
    Verifies NIC and internal network config.
    
3. **Ping Default Gateway**  
    `ping [router_IP]`  
    Tests connection to your router.
    
4. **Ping Another Local Device**  
    `ping [device_IP]`  
    Checks local network connectivity.
    
5. **Ping External Web Address**  
    `ping google.com`  
    Verifies internet access and DNS resolution.

