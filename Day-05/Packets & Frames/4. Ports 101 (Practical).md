# Ports 101 (Practical)

Ports 101 (Practical) refers to understanding how ports work in networking, particularly their role in communication between devices. In computer networking, ports are logical endpoints used for transmitting data between computers over a network. They are especially important for applications and protocols that need to communicate across different machines.

## What are Ports in Networking?
Ports are numerical identifiers used by the **Transport Layer** (Layer 4) of the OSI model, typically in conjunction with **IP addresses**. The combination of an **IP address** and a **port number** creates a unique identifier for a process or service on a device. This allows multiple applications to run simultaneously on a computer without interfering with each other.

Each port corresponds to a specific service or application, and different services use specific port numbers for communication. These ports are categorized into three ranges:

1. **Well-Known Ports (0–1023)**:
   - These are assigned to commonly used services and protocols, such as HTTP (port 80), FTP (port 21), and SSH (port 22). These ports are usually reserved and can only be used by system or root-level processes.

2. **Registered Ports (1024–49151)**:
   - These ports are assigned to software applications, services, and protocols by the Internet Assigned Numbers Authority (IANA). These ports are not reserved for any specific service but are typically used by non-system services like web servers (e.g., Apache) or game servers.

3. **Dynamic or Private Ports (49152–65535)**:
   - These ports are used dynamically by applications when establishing temporary communication sessions. These ports are typically used for client-side communication, especially when a client is connecting to a server (e.g., browser making HTTP requests).

 We have only briefly covered the more common protocols in cybersecurity. You can [find a table of the 1024 common ports listed](https://www.iana.org/assignments/service-names-port-numbers/service-names-port-numbers.xhtml) for more information.


## Key Practical Concepts for Ports:

### 1. **Port Numbers and Protocols**
   - **Port Number Assignment**: Port numbers help determine the destination service or application. When a packet arrives at a device, the transport layer (TCP/UDP) looks at the destination port number to decide which application should handle the incoming data.
   - **TCP vs. UDP**: Ports can be used by either **Transmission Control Protocol (TCP)** or **User Datagram Protocol (UDP)**. The difference is that TCP is connection-oriented (guarantees delivery and order) while UDP is connectionless (faster but no delivery guarantee).

### 2. **Common Port Numbers**
   - **HTTP (Port 80)**: Used for web traffic (standard, unsecured).
   - **HTTPS (Port 443)**: Used for secure web traffic.
   - **FTP (Port 21)**: Used for file transfers between clients and servers.
   - **SSH (Port 22)**: Used for secure shell connections, typically for remote administration.
   - **DNS (Port 53)**: Used for domain name system queries.
   - **SMTP (Port 25)**: Used for sending emails.
   - **POP3 (Port 110)**: Used by email clients to retrieve messages from a mail server.
   - **IMAP (Port 143)**: Used to retrieve email from a mail server, more advanced than POP3.

### 3. **Understanding Port Scanning**
   - **Port Scanning**: This is a technique used by network administrators and security professionals to check open ports on a network or a host to understand available services and assess vulnerabilities.
   - Common tools like **Nmap** are used for port scanning, where an attacker or an admin sends a request to each port to see if it responds. 
   - **Open Ports**: These are ports that are actively listening for incoming connections and may pose a security risk if not properly secured.
   - **Closed Ports**: These are ports that do not have any service listening on them. A closed port will reject or ignore incoming connection requests.

### 4. **How Ports Are Used in TCP/IP Communication**
   - **Client-Server Communication**: 
     - When a client (e.g., web browser) connects to a server, it uses a **source port** (randomly assigned by the operating system from the dynamic port range) and the destination port is a well-known port (e.g., port 80 for HTTP).
     - Example: A browser connecting to a website might use source port 20001 and destination port 80.
   
   - **Establishing Connections**: 
     - For TCP, the **three-way handshake** process establishes a connection between the client and server, specifying both source and destination port numbers for proper communication.
   
   - **Service Access via Ports**: 
     - Applications listen for incoming requests on specific ports. For example, a **web server** listens on port 80 (HTTP) or 443 (HTTPS), and a **file server** might listen on port 21 (FTP).
   
### 5. **Binding Ports**
   - When an application starts, it **binds** itself to a specific port. Binding means the application tells the operating system which port it will use to listen for incoming network connections. 
   - For example, when a web server starts up, it binds to port 80 for HTTP and port 443 for HTTPS.

### 6. **Dynamic vs. Static Ports**
   - **Dynamic Ports**: Temporary ports assigned by the operating system for a single session or connection (e.g., web browser to web server).
   - **Static Ports**: Fixed ports that are used by well-known services like HTTP (80), FTP (21), etc.

## Practical Examples:
1. **Web Browser Connecting to a Web Server**
   - Client: Source Port = 20001, Destination Port = 80
   - Server: Source Port = 80, Destination Port = 20001 (The server sends a response back to the client).

2. **SSH to a Remote Server**
   - Client: Source Port = 54321, Destination Port = 22 (SSH)
   - Server: Source Port = 22, Destination Port = 54321 (The server responds to the client’s SSH request).

3. **Port Scanning with Nmap**
   - Using a tool like Nmap, you can scan a range of ports (e.g., from 1 to 1024) to see which ports on a system are open and which services are available.

4. **Using Telnet to Test Ports**
   - You can use the **telnet** command to test if a port is open:
     ```bash
     telnet example.com 80
     ```
     This will try to connect to **example.com** on **port 80**. If successful, you will see a blank screen or a welcome message from the web server.

## Port Management and Security
- **Firewalls**: Firewalls can be configured to allow or block traffic on specific ports. For instance, a firewall may allow HTTP traffic on port 80 and block all other incoming traffic on non-essential ports.
- **Port Forwarding**: In network setups, port forwarding is used to direct external requests to the appropriate internal devices (e.g., forwarding port 80 requests to a web server inside a private network).
- **Port Blocking**: Ports that are known to be vulnerable to attacks (such as port 21 for FTP or port 23 for Telnet) are often blocked by firewalls for security purposes.

## Conclusion:
Understanding ports is crucial for configuring and troubleshooting network connections. Whether it's ensuring that services are accessible, securing open ports, or diagnosing network issues, knowledge of port functions and configurations is essential. Practically, this includes managing well-known ports, conducting port scans, binding ports to applications, and using firewalls to block or forward traffic appropriately.
