# What is the OSI Model?

The **OSI Model** (Open Systems Interconnection Model) is a conceptual framework that standardizes the functions of a network into **seven distinct layers**. Each layer serves a specific purpose and interacts with the layers directly above and below it. This model helps in understanding how data is transmitted across a network and provides a common language for designing and troubleshooting networking systems.

---

## The Seven Layers of the OSI Model:

1. **Physical Layer**  
   - Deals with the physical connection and transmission of raw data (bits) over a communication medium.  
   - Example: Cables, switches, and electrical signals.

2. **Data Link Layer**  
   - Ensures reliable transmission of data across the physical link by managing error detection, frame synchronization, and flow control.  
   - Example: MAC addresses, Ethernet.

3. **Network Layer**  
   - Responsible for routing data packets between devices across different networks and ensuring data reaches the correct destination.  
   - Example: IP addresses, routers, IPv4, IPv6.

4. **Transport Layer**  
   - Provides end-to-end communication, error correction, and reliable data delivery through protocols such as TCP and UDP.  
   - Example: TCP (Transmission Control Protocol), UDP (User Datagram Protocol).

5. **Session Layer**  
   - Manages and controls the dialogue between two devices, establishing, maintaining, and terminating sessions.  
   - Example: Maintaining a video call or logging into an online account.

6. **Presentation Layer**  
   - Translates data between the application layer and the transport layer, ensuring proper data formatting, encryption, and compression.  
   - Example: Encryption, data compression, and character encoding (ASCII, EBCDIC).

7. **Application Layer**  
   - The topmost layer that provides network services directly to end-users or applications. It interfaces with software
