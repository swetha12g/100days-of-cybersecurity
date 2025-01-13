# Networking and Related Concepts

## What is Networking?

**Networking** refers to the practice of connecting multiple devices, such as computers, servers, routers, and other hardware, in order to share data, resources, and services.  
The goal of networking is to enable communication between devices and to allow them to exchange information over various distances, whether:  
- **Locally**: Within a single building or campus.  
- **Globally**: Across the internet.  

---

## What is the Internet?

The **internet** is a global network of interconnected computers and servers that communicate with each other to share information, resources, and services.  
It allows devices like computers, smartphones, and tablets to connect with each other through a vast infrastructure of:  
- **Cables**  
- **Wireless signals**  
- **Satellites**

---

## Identifying Devices on a Network

Identifying devices on a network refers to the process of discovering and recognizing all the devices that are connected to a specific network.  
This is crucial for:  
- Network management.  
- Troubleshooting.  
- Security purposes.  

By identifying devices on a network, administrators can:  
- Ensure that only authorized devices are connected.  
- Monitor network performance.  
- Prevent potential security threats.  

### Methods for Identifying Devices:

#### 1. IP Addressing  
Each device on a network is typically assigned a **unique IP (Internet Protocol) address**. This address is used to identify the device and allows it to send and receive data on the network.  

Types of IP Addresses:  
- **IPv4**: A 32-bit address written as four numbers separated by periods (e.g., `192.168.1.1`).  
- **IPv6**: A newer, 128-bit address designed to replace IPv4, written in hexadecimal (e.g., `2001:0db8:85a3:0000:0000:8a2e:0370:7334`).  

Network administrators can identify devices by scanning the IP addresses in a network's address range.  

#### 2. MAC Address  
A **MAC (Media Access Control) address** is a unique hardware identifier assigned to network interfaces (e.g., Wi-Fi or Ethernet cards) on devices.  
- Unlike an IP address, the MAC address is **embedded into the hardware** and doesn’t change.  
- It is often used in **local area networks (LANs)** for device identification.  

Example: `00:14:22:01:23:45`.

---

## What is Ping?

**Ping** is a simple network utility used to test the connectivity between two devices on a network.  
It helps determine if one device (e.g., your computer or smartphone) can successfully communicate with another device (e.g., a server or another computer) over the network.  

### How Ping Works:
- **ICMP Protocol**: Ping uses the **Internet Control Message Protocol (ICMP)** to send a message called an **Echo Request** to a target device.  
- The target device then replies with an **Echo Reply**.  

The primary purposes of this message exchange are:  
- To check whether the target device is reachable.  
- To measure how long it takes for data to travel from one device to another (**latency** or **ping time**).  
