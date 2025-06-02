# Computer Networks: Key Concepts by Chapter

## Topic 1: Introduction to Computer Networks
-   **Computer Network Definition:** A collection of interconnected computers and devices that can share resources and information.
-   **Client-Server Model:** A network architecture where client devices request services and resources from a central server.
-   **Peer-to-Peer Model:** A network architecture where all devices (peers) have equal capabilities and can share resources directly without a central server.
-   **Local Area Network (LAN):** A network that connects computers and devices within a limited geographical area, such as a home or office building.
-   **Wide Area Network (WAN):** A network that spans a large geographical area, such as a country or continent, often connecting multiple LANs.
-   **Virtual Private Network (VPN):** Creates a secure, encrypted connection over a public network (like the Internet) to provide a private network experience.
-   **Protocols:** A set of rules and conventions that govern how data is exchanged between devices in a network.
-   **Network Architecture:** A framework that defines the layers, protocols, and services of a network.
-   **OSI Model:** A 7-layer conceptual framework that standardizes the functions of a telecommunication or computing system, including Physical, Data Link, Network, Transport, Session, Presentation, and Application layers.
-   **TCP/IP Model:** A 4-layer model widely used for Internet protocols, consisting of Link, Internet, Transport, and Application layers.
-   **Point-to-Point Transmission:** A direct connection between two network nodes.
-   **Broadcast Transmission:** A communication method where a single sender transmits data to all possible recipients on the network simultaneously.
-   **Multicast Transmission:** A communication method where data is sent from one sender to a specific group of interested receivers.
-   **Virtual LAN (VLAN):** A logical LAN that can group devices together even if they are on different physical network segments, configured on switches.
-   **Resource Sharing:** A primary use of networks, allowing users to share hardware (like printers), software, and data.

## Topic 2: Physical Layer
-   **Analog Signal:** A continuous signal where a time-varying feature (like voltage) represents some other time-varying quantity.
-   **Digital Signal:** A signal that represents data as a sequence of discrete values.
-   **Frequency (f):** The number of cycles a periodic signal completes per second, measured in Hertz (Hz).
-   **Bandwidth:** For physical channels, it refers to the range of frequencies a channel can transmit; in data communications, it often refers to the maximum data rate.
-   **Attenuation:** The reduction in signal strength as it travels through a transmission medium.
-   **Noise:** Unwanted electrical or electromagnetic energy that degrades the quality of signals and data.
-   **Twisted Pair Cable:** A common guided transmission medium consisting of pairs of insulated copper wires twisted together to reduce interference (e.g., UTP, STP).
-   **Coaxial Cable:** A guided medium with a central copper conductor, insulation, a braided metal shield, and an outer jacket, used for cable TV and early LANs.
-   **Fiber Optic Cable:** A guided medium that transmits data as pulses of light through thin strands of glass or plastic, offering high bandwidth and immunity to electromagnetic interference.
-   **Modulation:** The process of varying one or more properties (amplitude, frequency, phase) of a carrier signal to encode information.
-   **Multiplexing:** Combining multiple signals or data streams into a single channel for transmission (e.g., FDM, TDM).
-   **Frequency Division Multiplexing (FDM):** Divides the channel's bandwidth into separate frequency bands, allowing multiple signals to be transmitted simultaneously.
-   **Time Division Multiplexing (TDM):** Divides the channel into time slots, allocating each slot to a different user or signal in a round-robin fashion.
-   **Digital Subscriber Line (DSL):** A technology that provides digital data transmission over the wires of a local telephone network, with ADSL being a common asymmetric variant.
-   **Circuit Switching:** A switching method where a dedicated communication path (circuit) is established between two devices for the duration of the connection.

## Topic 3: Data Link Layer and MAC Sublayer
-   **Frame:** A unit of data at the Data Link Layer, consisting of a header, payload (Network Layer packet), and a trailer.
-   **Framing:** The process of dividing a stream of bits received from the network layer into manageable data units called frames.
-   **Error Detection:** Techniques used to identify if errors have occurred during data transmission, such as parity checks and checksums.
-   **Error Correction:** Techniques used to not only detect but also correct errors that occur during transmission, like Hamming codes.
-   **Flow Control:** Mechanisms that regulate the rate of data transmission between a sender and a receiver to prevent the receiver from being overwhelmed.
-   **Stop-and-Wait Protocol:** A simple flow control protocol where the sender transmits a frame and then waits for an acknowledgment (ACK) before sending the next frame.
-   **Sliding Window Protocol:** A flow control protocol that allows the sender to transmit multiple frames before needing an acknowledgment, improving efficiency over stop-and-wait.
-   **Piggybacking:** A technique where the acknowledgment for a received frame is sent along with an outgoing data frame in the reverse direction to save bandwidth.
-   **Medium Access Control (MAC) Sublayer:** A sublayer of the Data Link Layer responsible for controlling how devices in a network gain access to the medium and permission to transmit data.
-   **ALOHA (Pure and Slotted):** Early contention-based MAC protocols where stations transmit data whenever ready (Pure) or at the beginning of discrete time slots (Slotted).
-   **Carrier Sense Multiple Access (CSMA):** A MAC protocol where a station listens to the channel (carrier sense) before transmitting to avoid collisions.
-   **CSMA/CD (Collision Detection):** An enhancement to CSMA where stations can detect collisions while transmitting and then abort, wait a random time, and retry (used in classic Ethernet).
-   **CSMA/CA (Collision Avoidance):** A MAC protocol used in wireless networks (like Wi-Fi) where stations try to avoid collisions by using mechanisms like RTS/CTS before transmitting.
-   **Ethernet:** A widely used LAN technology that defines wiring and signaling standards for the physical layer, and MAC/framing for the data link layer.
-   **Spanning Tree Protocol (STP):** A network protocol that builds a loop-free logical topology for Ethernet networks by disabling redundant paths in a bridged network.

## Topic 4: Network Layer
-   **Internetworking:** The process of connecting different individual networks to form a larger network, enabling communication between devices on separate networks.
-   **Router:** A network layer device that forwards data packets between different computer networks based on their IP addresses.
-   **Tunneling:** A method of transporting packets of one protocol by encapsulating them within packets of another protocol, often used to connect IPv6 networks over an IPv4 infrastructure.
-   **Packet Fragmentation:** The process of breaking down a large IP packet into smaller fragments so that it can pass through a network with a smaller Maximum Transmission Unit (MTU).
-   **IP Address (IPv4):** A unique 32-bit numerical label assigned to each device participating in a computer network that uses the Internet Protocol for communication.
-   **Prefix (CIDR Notation):** A block of IP addresses defined by a network address and a prefix length (e.g., 192.168.1.0/24), used for efficient routing and IP address allocation.
-   **Subnetting:** The process of dividing a larger IP network into smaller, more manageable sub-networks (subnets).
-   **Network Address Translation (NAT):** A method of remapping an IP address space into another by modifying network address information in IP packet headers, commonly used to allow multiple devices on a private network to share a single public IP address.
-   **IP Version 6 (IPv6):** The successor to IPv4, providing a much larger 128-bit address space and other improvements.
-   **Internet Control Message Protocol (ICMP):** A supporting protocol in the Internet protocol suite used by network devices to send error messages and operational information (e.g., destination unreachable, time exceeded).
-   **Address Resolution Protocol (ARP):** A protocol used to map an IP address to a physical (MAC) address on a local network.
-   **Dynamic Host Configuration Protocol (DHCP):** A network management protocol used to automatically assign IP addresses and other network configuration parameters to devices on a network.
-   **Autonomous System (AS):** A collection of connected IP routing prefixes under the control of one or more network operators that presents a common, clearly defined routing policy to the Internet.
-   **Open Shortest Path First (OSPF):** An interior gateway protocol (IGP) used for routing within a single autonomous system, based on link-state routing.
-   **Border Gateway Protocol (BGP):** An exterior gateway protocol (EGP) used for routing between autonomous systems on the Internet, focusing on path selection based on policies.

## Topic 5: Transport Layer
-   **Process-to-Process Delivery:** The transport layer is responsible for providing logical communication between application processes running on different hosts.
-   **Transport Entity:** The hardware or software component within the transport layer that performs its functions, located in the OS kernel, a library, or NIC.
-   **Connection-Oriented Service:** A transport service that establishes a dedicated connection before data transfer, ensures reliable delivery, and then releases the connection (e.g., TCP).
-   **Connectionless Service:** A transport service that sends data without establishing a prior connection; packets may arrive out of order or be lost (e.g., UDP).
-   **Transport Layer Primitives:** Operations provided to application programs to access transport layer services, such as LISTEN, CONNECT, SEND, RECEIVE, DISCONNECT.
-   **Socket:** An endpoint for communication, identified by an IP address and a port number, used by processes to send and receive data.
-   **Port Number:** A 16-bit number that helps identify a specific process to which an Internet or other network message is to be forwarded when it arrives at a server.
-   **User Datagram Protocol (UDP):** A simple, connectionless transport protocol that provides fast but unreliable data transmission with minimal overhead.
-   **UDP Header:** Contains Source Port, Destination Port, UDP Length, and UDP Checksum fields.
-   **Transmission Control Protocol (TCP):** A connection-oriented transport protocol that provides reliable, ordered, and error-checked delivery of a stream of bytes between applications.
-   **TCP Segment Header:** Contains fields like Source Port, Destination Port, Sequence Number, Acknowledgment Number, Flags (SYN, ACK, FIN, RST, PSH, URG), Window Size, and Checksum.
-   **Three-Way Handshake:** The process TCP uses to establish a connection, involving the exchange of SYN and ACK segments between client and server.
-   **TCP Sliding Window:** A flow control mechanism where the receiver specifies the amount of data (window size) it is willing to receive, allowing the sender to transmit multiple segments before waiting for an acknowledgment.
-   **TCP Congestion Control:** Mechanisms used by TCP to prevent network congestion by adjusting the rate at which data is sent, using algorithms like Slow Start and Fast Recovery.
-   **Real-Time Transport Protocol (RTP):** A protocol often used with UDP for delivering audio and video over IP networks, providing features like sequence numbering and timestamping for real-time applications.

## Topic 6: Application Networking Services
-   **Domain Name System (DNS):** A hierarchical and distributed naming system that translates human-readable domain names (e.g., www.google.com) into machine-readable IP addresses.
-   **DNS Resolver:** A client-side library procedure that an application program calls to look up an IP address for a given domain name.
-   **DNS Name Server:** A server that stores DNS resource records and responds to queries from resolvers.
-   **Resource Record (RR):** An entry in the DNS database that provides information about a domain, such as its IP address (A or AAAA record) or mail server (MX record).
-   **Electronic Mail (Email):** A system for exchanging digital messages between users over a network.
-   **User Agent (UA):** An email client application that allows users to compose, send, receive, and manage emails (e.g., Outlook, Gmail).
-   **Message Transfer Agent (MTA):** A mail server software that relays emails from senders to recipients using SMTP.
-   **Simple Mail Transfer Protocol (SMTP):** The standard protocol for sending email messages between servers and for submitting emails from a user agent to a mail server (typically uses TCP port 25).
-   **Internet Message Access Protocol (IMAP):** A protocol that allows a user agent to access and manage emails stored on a mail server, providing more advanced features than POP3 like folder management on the server (typically uses TCP port 143).
-   **World Wide Web (WWW):** A global information system where documents and other web resources are identified by Uniform Resource Locators (URLs), interlinked by hypertext, and accessible via the Internet.
-   **HyperText Transfer Protocol (HTTP):** The foundation protocol for data communication for the World Wide Web, used by web browsers to request web pages from web servers (typically uses TCP port 80).
-   **Uniform Resource Locator (URL):** A reference (an address) to a resource on the Internet, specifying its location and the protocol to retrieve it (e.g., http://www.example.com/page.html).
-   **Web Browser:** A software application used to access and display information on the World Wide Web (e.g., Chrome, Firefox).
-   **MIME (Multipurpose Internet Mail Extensions) Type:** A standard that indicates the nature and format of a document, file, or assortment of bytes, used by browsers to determine how to handle web content.
-   **Cookies:** Small pieces of data stored on a user's computer by their web browser while Browse a website, used by servers to remember stateful information or track Browse activity.

## Topic 7: Network Management
-   **Firewall:** A network security device that monitors and filters incoming and outgoing network traffic based on an organization's predefined security policies.
-   **Packet Filter:** A type of firewall that inspects individual packets and allows or blocks them based on rules defined by IP addresses, ports, and protocols.
-   **DeMilitarized Zone (DMZ):** A perimeter network that protects an organization's internal local-area network (LAN) from untrusted traffic, often hosting externally accessible services like web or email servers.
-   **Stateful Firewall:** A firewall that keeps track of the state of active connections and uses this information to make filtering decisions, offering more security than simple packet filters.
-   **Application-Level Gateway (Proxy Firewall):** A firewall that inspects traffic at the application layer, allowing for more granular control and understanding of application-specific commands and data.
-   **Virtual Private Network (VPN) - Security Context:** A technology that creates a secure, encrypted connection (tunnel) over a less secure network, such as the internet, often used to connect remote users or sites to a private network.
-   **ISO Network Management Framework (FCAPS):** A model that categorizes network management into five functional areas: Fault, Configuration, Accounting, Performance, and Security management.
-   **Fault Management:** The process of detecting, isolating, diagnosing, and correcting network faults to ensure continuous operation.
-   **Configuration Management:** The process of identifying, controlling, and maintaining the configuration of network devices and services.
-   **Accounting Management:** The process of tracking network resource usage by users for billing, capacity planning, and cost allocation.
-   **Performance Management:** The process of monitoring and controlling network performance to ensure services are delivered efficiently and meet quality objectives, involving monitoring and tuning.
-   **Security Management (Network Context):** The process of protecting network resources and information from unauthorized access, modification, or denial of service, including managing security services and reporting security events.
-   **Simple Network Management Protocol (SNMP):** An application-layer protocol used for managing and monitoring network devices on an IP network, involving managers, agents, and MIBs.
-   **Management Information Base (MIB):** A hierarchical database of managed objects on a network device that an SNMP agent can access and an SNMP manager can query or set.
-   **SNMP PDU (Protocol Data Unit):** The message format used in SNMP communications, such as GETREQUEST, SETREQUEST, RESPONSE, and TRAP, to exchange management information.

## Topic 8: Software Defined Networks (SDN)
-   **Data Plane (Forwarding Plane):** The part of a network device responsible for forwarding packets based on decisions made by the control plane; it handles tasks like packet buffering, scheduling, and header modification.
-   **Control Plane:** The part of a network device responsible for making decisions about where traffic is sent, such as routing protocol computations and updating the forwarding table.
-   **Management Plane:** The part of a network device used by network administrators to configure, monitor, and manage the network and its devices.
-   **Software Defined Networking (SDN):** An network architecture approach that decouples the network control plane from the data (forwarding) plane, allowing network control to become directly programmable and the underlying infrastructure to be abstracted for applications and network services.
-   **Plane Separation:** A fundamental characteristic of SDN where the control logic is removed from network hardware and given to a centralized controller.
-   **Centralized Control:** In SDN, a software-based controller manages network devices, providing a global view of the network and simplifying device functionality.
-   **Northbound API:** In SDN, an interface provided by the controller that allows applications to program network behavior and access network information.
-   **Southbound API:** In SDN, an interface between the controller and the network devices (data plane) that allows the controller to program the forwarding behavior of these devices (e.g., OpenFlow).
-   **SDN Controller:** The "brain" of an SDN network that maintains a centralized view of the network, implements policies, and instructs data plane devices on how to forward traffic.
-   **SDN Device (Switch):** A network device in an SDN architecture that primarily performs packet forwarding based on instructions received from the SDN controller via a southbound API.
-   **OpenFlow:** A prominent southbound API and protocol that enables an SDN controller to interact with the forwarding plane of network switches and routers to modify how network packets are processed and routed.
-   **Flow Table:** A table within an OpenFlow-enabled switch that contains rules (flow entries) telling the switch how to process packets matching specific criteria.
-   **SDN Applications:** Software programs that run on top of the SDN controller (via the northbound API) to provide specific network functions or services, like load balancing or security monitoring.
-   **Network Automation:** SDN facilitates the automation of network configuration, management, and provisioning tasks through programmable control.
-   **Network Virtualization (in SDN context):** SDN can enable the creation of multiple virtual networks, each with its own policies and forwarding logic, over a shared physical infrastructure, often managed by the controller.
