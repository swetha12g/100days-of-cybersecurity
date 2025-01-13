# Introducing LAN Topologies: Basics of Local Area Network Structures

In computer networking, LAN topologies refer to the layout or organizational structure of devices (nodes) in a 
Local Area Network (LAN). The topology defines how nodes, such as computers, switches, and routers, are connected and how they communicate with each other. The choice of topology affects the network's performance, scalability, cost, and fault tolerance.

## Types of LAN Topologies : 

## Bus Topology :

#### Structure: 

All devices are connected to a single central cable (the "bus") using T-connectors or taps.

#### Communication: 

Data travels in both directions along the bus until it reaches its destination.

### Advantages:

1. Cost-effective and easy to set up for small networks.

2. Minimal cabling required.

### Disadvantages:

1. A single point of failure (the central cable) can bring down the entire network.

2. Performance degrades as more devices are added.

## Star Topology :

#### Structure: 

All devices are connected to a central hub or switch.

#### Communication: 

Devices communicate indirectly via the hub/switch, which acts as a relay.

### Advantages:

1. Easy to add or remove devices without affecting the network.

2. Failure of a single device does not impact the rest of the network.

### Disadvantages:

1. The central hub/switch is a single point of failure.

2. More cabling is required compared to bus topology.

## Ring Topology :

#### Structure: 

Devices are connected in a closed loop, with each device connected to two others.

#### Communication: 

Data travels in one direction (unidirectional) or both directions (bidirectional) around the ring.

### Advantages:

1. Equal access to resources, reducing data collision issues.

2. Predictable performance under heavy traffic.

### Disadvantages:

1. A failure in any single connection can disrupt the network.

2. Troubleshooting is more complex than with bus or star topologies.
_______________________________________________________________________________________________________________________________________________________________

# A Primer on Subnetting :

Subnetting is the process of dividing a large network into smaller, more manageable networks called subnets. It helps improve network efficiency, enhance security, and optimize IP address allocation by assigning smaller groups of addresses to specific segments or devices within the network.

## Subnets use IP addresses in three different ways:

### Network Address:

Identifies the specific subnet within a larger network and is used to route traffic to the correct subnet.

### Host Addresses:

Assigned to devices within the subnet, allowing them to communicate within and outside the network.

### Default Gateway : 

The default gateway in subnetting is the IP address of a router or a network device that acts as the access point for a subnet to communicate with other networks or subnets. It serves as the "exit point" for traffic destined for addresses outside the local subnet.
__________________________________________________________________________________________________________________________________________________________________

# Address Resolution Protocol :

Address Resolution Protocol (ARP) is a network protocol used to map an IP address to a device's physical MAC (Media Access Control) address within a local network. When a device needs to communicate with another device on the same network, ARP helps find the corresponding MAC address by sending a broadcast request, ensuring proper delivery of data packets.

## ARP Request : 

An ARP Request is a broadcast packet sent by a device on a local network to discover the MAC address associated with a specific IP address. The request contains the sender's IP and MAC addresses and the target IP address but leaves the target MAC address field blank.

### Example:

#### Device A (192.168.1.10) sends a broadcast:

`` "Who has 192.168.1.20? Tell 192.168.1.10." ``

## ARP Reply :

An ARP Reply is a unicast response sent by the device with the matching IP address, providing its MAC address directly to the requesting device. The reply allows the requester to store the MAC-IP mapping in its ARP cache for future use.

### Example:

#### Device B (192.168.1.20) responds to Device A:

`` "192.168.1.20 is at AA:BB:CC:DD:EE:FF." ``
_________________________________________________________________________________________________________________________________________________________________

# Dynamic Host Configuration Protocol :

DHCP (Dynamic Host Configuration Protocol) is a protocol used in networks to automatically assign IP addresses to devices (such as computers, phones, and printers) when they connect to the network. It allows network administrators to manage IP address allocation efficiently, without needing to manually configure each device. When a device joins the network, the DHCP server provides it with an available IP address, subnet mask, default gateway, and DNS server information, ensuring smooth communication between devices on the network.

The DHCP process involves three key steps: DHCP Discover, DHCP Offer, and DHCP ACK. Here's a basic explanation of each:

## DHCP Discover : 

When a device (client) joins a network, it sends a DHCP Discover message to locate available DHCP servers. This message is broadcasted to all devices on the local network since the client does not yet have an IP address.

## DHCP Offer : 

When a DHCP server receives the Discover message, it responds with a DHCP Offer. This message contains an available IP address, subnet mask, lease time, and other network configuration details that the server is offering to the client.

## DHCP ACK : 

After receiving the Offer, the client sends a DHCP Request to the server to confirm the IP address and settings. The server then sends a DHCP ACK (Acknowledgment), which finalizes the IP assignment. At this point, the client can begin using the provided IP address to communicate on the network. This process ensures devices are automatically configured with proper network settings without requiring manual intervention.
