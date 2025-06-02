# Computer Networks Content Guide

This guide outlines the key concepts covered in each topic of your Computer Networks course, based on the provided lecture notes.

## Topic 1: Introduction to Computer Networks

This introductory chapter lays the groundwork for understanding computer networks.

### Core Concepts:
-   **Definition of a computer network:** A set of computers sharing resources.
-   **Network nodes:** Redistribution points or communication endpoints.
-   **Uses of Computer Networks:**
    -   **Resource Sharing:**
        -   **Client-Server Model:** Service provided by a server, client initiates communication by sending requests. Examples include web Browse (Firefox and a web server).
        -   **Peer-to-Peer Model:** No special server entities; peers contribute resources equally. Example: Bitcoin network.
    -   **Applications:** Video conferencing (Zoom), Social Networks (Facebook), Email, Instant Messaging (WhatsApp), eCommerce (Uber, PickMe).
    -   **Mobile Users:**
        -   Connectivity (WiFi, GSM, 3G/4G/5G, Bluetooth)
        -   Devices (Smartphones, Smartwatches)
        -   Applications (Navigation, Fitness monitoring).
    -   **Sensor Networks:** Small sensors gather physical world data (temperature, humidity, position). Smartphones themselves act as sensor nodes (Camera, GPS, Accelerometer).
    -   **Social Issues:** Privacy violations, fake news, social engineering (phishing).

### Network Hardware and Software:
-   **Network Classification based on Transmission Technology:**
    -   **Point-to-Point (Unicast):** One computer connected to another (e.g., fiber link from home to telecom provider).
    -   **Broadcast:** Communication channel shared by all computers (e.g., WiFi networks).
    -   **Multicast:** Transmit to a subset of computers.
-   **Network Classification based on Scale:**
    -   **Personal Area Networks (PAN):** Communication over the range of a person (e.g., Bluetooth connecting headset to phone).
    -   **Local Area Networks (LAN):** Operates within a single building (home, office).
        -   **Wireless (WiFi - 802.11):** Devices connect via an Access Point.
        -   **Wired (Ethernet):** Devices connect to a Hub or Switch.
            -   **Hub:** Receives a packet and sends it to all other ports.
            -   **Switch:** Relays a packet to another port based on the destination address.
        -   **Virtual LAN (VLAN):** Divides one physical LAN into several logical LANs by assigning "colors" (identifiers) to switch ports.
    -   **Metropolitan Area Networks (MAN):** Covers a city, connects LANs (e.g., Metro Ethernet).
    -   **Wide Area Networks (WAN):** Spans a large geographical area (country, continent), often using leased lines from telecommunication providers. The Internet is an example of a WAN.
    -   **Virtual Private Network (VPN):** Creates a virtual link over a public network (like the Internet) with data encryption.

### Protocols and Layering:
-   **Protocol:** An agreement between communicating parties, implemented in hardware or software.
-   **Network Architecture:** A set of layers and protocols.
-   **Design Issues for Layers:**
    -   Error Detection and Correction.
    -   Routing: Finding a suitable path to the destination.
    -   Addressing and Naming: Identifying recipients.
    -   Quality of Service.
-   **Network Reference Models:**
    -   **OSI Model (7 layers):** Physical, Data Link, Network, Transport, Session, Presentation, Application.
    -   **TCP/IP Model (4 layers):** Link, Internet, Transport, Application.
    -   **Textbook Model (5 layers):** Physical, Link, Network, Transport, Application.
-   **Metric Units:** Distinction between units based on powers of 10 (networks) and powers of 2 (storage). (B for Bytes, b for bits).

## Topic 2: Physical Layer

This chapter delves into the physical means of transmitting data.

### Signals and Their Properties:
-   **Signal:** A time-varying voltage, current, or electromagnetic wave carrying information.
-   **Analog Signal:** Continuous signal where a time-varying feature represents another time-varying quantity.
-   **Digital Signal:** Represents data as a sequence of discrete values (e.g., square wave).
-   **Properties of Signals (illustrated with Sine Waves):**
    -   **Amplitude:** Maximum voltage/intensity of the signal.
    -   **Period (T):** Time for one complete cycle of a periodic signal.
    -   **Frequency (f):** Number of cycles per second (Hz). `f=1/T`.
    -   **Wavelength (λ):** Distance between two consecutive maxima/minima. `λ=c/f` (where c is propagation speed).
    -   **Phase:** The position of a point in time on a waveform cycle. Phase difference describes the shift between two signals.
-   **Transmission Impairments:**
    -   **Attenuation:** Loss of signal strength.
    -   **Amplification (Distortion):** While not a problem, the output signal differs from the input if not done perfectly.
    -   **Delay:** Signal arrives later than expected.
    -   **Noise:** Unwanted signals distorting the original signal.
-   **Fourier Analysis (Summing Up Sine Waves):**
    -   Complex periodic signals (like square waves) can be decomposed into a sum of simple sine waves of different frequencies, amplitudes, and phases.
    -   A digital signal is a combination of an infinite number of sine waves.

### Transmission Media:
-   **Channel:** Physical transmission medium or logical connection.
-   **Maximum Data Rate of a Channel:**
    -   **Bandwidth:** For Electrical Engineers, a range of frequencies (Hz); for Computer Scientists, the maximum data rate (Bits/sec). All physical channels are bandwidth-limited.
    -   **Nyquist Theorem (Noiseless Channel):** Max Data Rate = `2B log₂(V)` Bits/sec (B=bandwidth in Hz, V=number of discrete signal levels).
    -   **Shannon Capacity (Noisy Channel):** Max Data Rate = `B log₂(1+S/N)` Bits/sec (S/N = Signal-to-Noise Ratio).
    -   **Signal-to-Noise Ratio (SNR):** S/N, often expressed in decibels (dB): `10 log₁₀(S/N)` dB.
-   **Guided Transmission Media:**
    -   **Twisted Pairs:** Two insulated copper wires twisted together. The difference in voltages represents the signal; twisting helps cancel out noise.
        -   **Shielded Twisted Pair (STP):** Includes shielding to reduce interference.
        -   **Unshielded Twisted Pair (UTP):** No shielding.
        -   **Categories:** Cat 3 (16 MHz), Cat 5 (100 MHz), Cat 6 (250-500 MHz), Cat 7 (STP, up to 1000 MHz).
    -   **Coaxial Cables:** Stiff copper core, insulator, cylindrical conductor (braided mesh), protective sheath. Used for TV antenna connections; bandwidth up to a few GHz.
    -   **Powerline Communication:** Uses household electrical wiring for data transmission (up to 100 Mbps).
    -   **Optical Transmission Systems (Fiber Optics):**
        -   **Components:** Light source (LED, Semiconductor laser), transmission medium (fiber cable), detector (photodiode).
        -   **Transmission Medium:** Glass/silica fibers; light trapped by total internal reflection.
        -   **Multimode Fiber:** Wider core, light rays bounce at different angles, less expensive, for shorter distances.
        -   **Single-Mode Fiber:** Very narrow core, light propagates straight, expensive, for longer distances.
        -   **Structure:** Core (glass), Cladding (glass), Jacket (plastic).
-   **Wireless Transmission Media:**
    -   **Electromagnetic Waves:** Characterized by frequency (f), wavelength (λ), and propagation speed (c). `c=fλ`.
    -   **Electromagnetic Spectrum:** Radio waves, microwaves, infrared, visible light, UV, X-rays, Gamma rays. Different parts are used for different communication types (AM/FM radio, TV, satellite, fiber optics).
    -   **Regulations:** Bodies like TRCSL (Sri Lanka), FCC (USA), ITU manage spectrum allocation.
    -   **ISM Bands (Industrial, Scientific, Medical):** Unlicensed bands for devices like garage door openers, WiFi, Bluetooth, microwaves.
    -   **Infrared:** Short-range (TV remotes), cannot penetrate walls.
    -   **Free-space Optical Communication (LiFi):** High-speed data transmission using visible light, UV, or infrared. Useful in EMI-sensitive environments.

### Modulation and Multiplexing:
-   **Modulation:** Varying properties (amplitude, frequency, phase) of a carrier signal with a modulation signal containing information.
-   **Digital Modulation:** Converting bits into signals.
    -   **Baseband Transmission:** Directly converts bits to signals (e.g., NRZ, NRZI, Manchester, Bipolar).
    -   **Passband Transmission:** Modulates a carrier signal (e.g., Amplitude Shift Keying - ASK, Frequency Shift Keying - FSK, Phase Shift Keying - PSK).
-   **Multiplexing:** Combining multiple signals into one over a shared medium using a Multiplexer (MUX) and Demultiplexer (DEMUX).
    -   **Frequency Division Multiplexing (FDM):** Divides spectrum into frequency bands with guard bands.
    -   **Time Division Multiplexing (TDM):** Each user gets a time burst (slot) in a round-robin fashion, with guard times.
    -   **Statistical Time Division Multiplexing (STDM):** Slots allocated on demand (related to packet switching).

### Public Switched Telephone Network (PSTN) and Access Technologies:
-   **PSTN:** Originally for voice; Local Loop (analog twisted pairs, 3100 Hz bandwidth) and Trunks (digital fiber optics).
-   **Modems (Modulator-Demodulator):** Convert digital bits to analog signals for local loop transmission and vice-versa.
-   **Digital Subscriber Line (DSL):** Uses the full bandwidth (approx. 1.1 MHz) of the local loop by removing filters.
    -   Bandwidth divided into 256 channels (4312.5 Hz each). Channel 0 for POTS, channels 1-5 unused, 250 for data/control.
-   **Asymmetric Digital Subscriber Line (ADSL):** More channels allocated for downstream than upstream. Equipment includes splitter and ADSL modem at customer premises, DSLAM at telephone company end office.
-   **Fiber to the Home (FTTH):** Uses Passive Optical Networks (PON).
    -   Optical Splitter/Combiner used.
    -   Optical Network Terminal (ONT) at home converts optical to electrical signals and vice-versa, also acts as MUX/DEMUX.

### Switching:
-   **Circuit Switching:** Dedicated communication channel (circuit) established for the duration of a session (e.g., analog telephone network). Full bandwidth available.
    -   **Advantages:** Dedicated bandwidth, continuous transfer.
    -   **Disadvantages:** Bandwidth may be underutilized.
-   **Packet Switching:** Data grouped into packets (header + payload).
    -   **Connectionless Packet Switching:** Packets routed individually based on header info; no pre-established path.
    -   **Connection-Oriented Packet Switching:** Setup phase establishes a virtual circuit; packets have a connection identifier.

## Topic 3: Data Link Layer and MAC Sublayer

This chapter focuses on reliable data transfer between adjacent network nodes and controlling access to shared media.

### Design Issues for Data Link Layer:
-   Uses services of the physical layer to send/receive bits.
-   **Functions:**
    -   Providing a well-defined service interface to the network layer.
    -   Dealing with transmission errors.
    -   Regulating data flow (preventing slow receivers from being swamped).
-   **Packet and Frame Relationship:** The data link layer encapsulates a network layer packet into a frame (Header, Payload, Trailer).
-   **Services Provided to the Network Layer:**
    -   **Unacknowledged Connectionless Service:** Frames sent without acknowledgment (e.g., Ethernet).
    -   **Acknowledged Connectionless Service:** Each frame acknowledged; retransmission if no ACK (e.g., WiFi).
    -   **Acknowledged Connection-Oriented Service:** Connection established before data transfer; guarantees each frame is received.
-   **Framing:**
    -   Defining start and end of frames.
    -   Breaking bit stream into frames and computing a checksum for each.
    -   Destination recalculates checksum to detect errors.
-   **Error Control:**
    -   Prevents frame duplication.
    -   Uses positive/negative acknowledgments or timeouts for retransmission.
-   **Flow Control:**
    -   Ensuring sender doesn't overwhelm receiver's buffer.

### Error Detection and Correction Strategies:
-   **Error-Correcting Codes:** Include enough redundancy for the receiver to deduce original data (e.g., Hamming codes).
-   **Error-Detecting Codes:** Include enough redundancy to detect errors and request retransmission (e.g., Parity, Checksums).
    -   **Parity:** Adds a bit to make the number of 1s even or odd. Can detect single-bit errors. (Example provided).
    -   **Checksum:** Calculated sum sent with data; receiver recalculates to verify.
    -   **Checksum Example (RFC1071):** Data as 16-bit integers, sum calculated (carry wraps around), 1's complement of sum is checksum. Validation involves summing data and checksum; result should be all 1s. (4-bit example provided).
-   **Error Correcting Codes & Hamming Distance:**
    -   **Hamming Distance:** Number of bit positions in which two codewords differ.
    -   To detect 'd' errors, a distance `d+1` code is needed.
    -   To correct 'd' errors, a distance `2d+1` code is needed.
    -   (Example of determining differing bits using XOR).
-   **Hamming Code:** Uses multiple parity bits.
    -   Equation for number of parity bits (P) for 'n' data bits: `2^P >= n+P+1`.
    -   Parity bits placed at positions that are powers of 2 (1, 2, 4, 8...).
    -   Each parity bit covers specific data bit positions.
    -   (Example with data 11001 (n=5), P=4).

### Elementary Data Link Protocols:
-   **Utopian Simplex Protocol:** Unidirectional, always ready, infinite buffer, no errors.
-   **Simplex Stop-and-Wait Protocol (Error-Free Channel):** Sender sends one frame, waits for ACK to prevent flooding.
-   **Simplex Stop-and-Wait Protocol (Noisy Channel):** Handles damaged/lost frames using ACKs and timeouts for retransmission. Uses sequence numbers to handle duplicate data due to lost ACKs.

### Sliding Window Protocols:
-   For full-duplex data transmission.
-   **Piggybacking:** Attaching ACKs to outgoing data frames to save bandwidth. If no data frame soon, a separate ACK is sent.
-   Frames contain sequence numbers (0 to `2^n - 1`).
-   **Sending Window:** Set of sequence numbers sender is permitted to send (sent but not yet ACKed).
-   **Receiving Window:** Set of frames receiver is permitted to accept. Accepted frames buffered; window rotates when frame at lower edge is passed to network layer.

### Medium Access Control (MAC) Sublayer:
-   **Channel Allocation Problem:** How to allocate a single broadcast channel among competing users.
-   **Static Channel Allocation:**
    -   **Frequency Division Multiplexing (FDM):** Bandwidth divided into N portions for N users.
    -   **Time Division Multiplexing (TDM):** Each user gets every Nth time slot.
    -   Inefficient for bursty computer traffic.
-   **Dynamic Channel Allocation Assumptions:** Independent traffic, single channel, observable collisions, continuous or slotted time, carrier sense or no carrier sense.
-   **Multiple Access Protocols:**
    -   **Pure ALOHA:** Users transmit whenever they have data. Collisions occur. Senders detect collisions (e.g., by listening to hub's rebroadcast) and retransmit after a random time. (Visual example).
        -   Efficiency: Throughput `S = G * e^(-2G)`. Max throughput is `1/(2e)` at `G=0.5`.
    -   **Slotted ALOHA:** Transmission only at the beginning of a time slot. Halves vulnerable period. (Visual example).
        -   Efficiency: Throughput `S = G * e^(-G)`. Max throughput is `1/e` at `G=1`.
        -   (Comparison graph of Pure vs. Slotted ALOHA).
    -   **Carrier Sense Multiple Access (CSMA) Protocols:** Stations listen for a carrier before transmitting.
        -   **1-Persistent CSMA:** If channel idle, transmit. If busy, wait until idle then transmit with probability 1.
        -   **Non-Persistent CSMA:** If channel idle, transmit. If busy, wait random time, then repeat.
        -   **P-Persistent CSMA:** For slotted channels. If idle, transmit with probability p; defer with probability q=1-p to next slot.
    -   **CSMA/CD (Collision Detection):** Stations detect collisions and stop transmitting. Basis of classic Ethernet. (Visual example).

### Ethernet:
-   **Frame Format (DIX Ethernet vs. IEEE 802.3):** Preamble, Destination Address, Source Address, Type/Length, Data, Pad, Checksum.
-   **MAC Sublayer Protocol Details:**
    -   **Preamble** (8 bytes, `10101010` pattern, last byte is Start of Frame delimiter for 802.3 with last 2 bits `11`).
    -   **Destination/Source Address** (6 bytes each, globally unique, OUI for first 3 bytes).
    -   **Type** (Ethernet) / **Length** (IEEE 802.3).
    -   **Pad:** Fills frame to minimum size.
    -   **Checksum** (CRC).
-   **Switched Ethernet:**
    -   Hubs are logically like a single cable; capacity shared.
    -   Switches improve this with a high-speed backplane connecting ports.
    -   Switches output frames only to destined ports, check Ethernet address.
    -   No collisions in a switch; can send multiple frames simultaneously.
-   **Fast Ethernet (IEEE 802.3u):** Speeds > 100 Mbps. Uses Twisted Pair (`100Base-T4`, `100Base-TX`) and Fiber (`100Base-FX`).
-   **Gigabit Ethernet (IEEE 802.3ab):** Speeds up to 1 Gbps. Uses Twisted Pair (`1000Base-CX`, `1000Base-T`) and Fiber (`1000Base-SX`, `1000Base-LX`).
-   **10-Gigabit Ethernet:** Speeds up to 10 Gbps. Uses Twisted Pair (`10GBase-CX4`, `10GBase-T`) and Fiber (`10GBase-SR`, `-LR`, `-ER`).

### Wireless LANs (WLANs):
-   Often use Access Points connected with copper wires.
-   Cannot easily identify collisions compared to wired LANs.
-   Transmitted frames received by all stations.
-   Use CSMA to listen and send.
-   **Issues:**
    -   **Hidden Terminal Problem:** Station A transmits to B. C is out of A's range but in B's range. If C transmits to B while A is transmitting, collision at B.
    -   **Exposed Terminal Problem:** B transmits to A. C wants to transmit to D. C senses B's transmission and defers, even though C-D transmission wouldn't interfere with B-A.
-   **802.11 Architecture and Protocol Stack:**
    -   **Modes:** Infrastructure mode (uses Access Point), Ad-hoc mode (direct peer-to-peer).
    -   Data Link Layer split: MAC sublayer (channel allocation) and LLC sublayer (hides 802 variant differences from upper layers).
-   **802.11 Physical Layer:** Uses short-range radios in 2.4 GHz or 5 GHz ISM bands.
    -   `802.11b`: up to 11 Mbps.
    -   `802.11a`: up to 54 Mbps (5 GHz).
    -   `802.11n`: up to 600 Mbps (uses MIMO - Multiple Input Multiple Output).
    -   Other standards: `802.11ac`, `ad`, `af`, `ah`, `ax`.
-   **802.11 MAC Sublayer Protocol:**
    -   Different from Ethernet due to:
        -   Nearly half-duplex communication (cannot transmit and listen for noise simultaneously on one frequency). Uses CSMA/CA (Collision Avoidance).
        -   Different transmission ranges leading to hidden/exposed terminal problems.
    -   Uses Request to Send (RTS) and Clear to Send (CTS) frames to mitigate these problems.

### Data Link Layer Switching:
-   **Bridges (Switches):** Connect multiple LANs or split a single LAN. Operate at Data Link Layer, examine DL address to forward frames.
    -   Maintain a table of destinations and ports, learned via flooding algorithms.
-   **Spanning Tree Protocol (STP):** Used to prevent loops when redundant links exist between bridges by ignoring some connections.
-   **Device Layers:** Application Gateway (Application), Transport Gateway (Transport), Router (Network), Bridge/Switch (Data Link), Hub/Repeater (Physical).
-   **Virtual LANs (VLANs):** Solution to avoid physical rewiring when network structure changes. Configuration table in bridge defines which port belongs to which VLAN.

## Topic 4: Network Layer

This chapter covers how data is routed across networks from source to destination.

### Internetworking:
-   Connecting different types of networks (e.g., Ethernet, MPLS, 802.11).
-   **How Networks Differ:** Service offered (connectionless/connection-oriented), addressing, broadcasting, packet size, ordering, QoS, reliability, security, parameters, accounting.
-   **Connecting Networks:**
    -   Translation devices (not scalable).
    -   Common layer on top (e.g., IP).
-   **Interconnection devices:** Routers (operate at Network Layer).
-   **Tunneling:** Encapsulating packets of one protocol (e.g., IPv6) within packets of another (e.g., IPv4) to traverse an incompatible network.
-   **Internetwork Routing:**
    -   Requires two levels: Intradomain (within an Autonomous System) and Interdomain (between ASes).
    -   **BGP (Border Gateway Protocol)** is the interdomain protocol for the Internet, making each connected network an Autonomous System (AS).
-   **Packet Fragmentation:** Handling different Maximum Transmission Units (MTUs) across networks.
    -   Transparent fragmentation (overhead on routers).
    -   Non-transparent fragmentation (source fragments, higher network overhead potentially). IP uses this.
-   **Path MTU Discovery:** Modern approach to avoid fragmentation by discovering the minimum MTU along a path.

### Network Layer in the Internet:
-   **Design Principles for Network Protocols:** Make it work, keep it simple, clear choices, modularity, expect heterogeneity, avoid static options, good design (not perfect), strict sending/tolerant receiving, scalability, performance/cost.
-   **IP Version 4 (IPv4):**
    -   **Header Fields:** Version, IHL (Internet Header Length), Differentiated Services, Total Length, Identification, Flags (DF, MF), Fragment Offset, Time To Live (TTL), Protocol, Header Checksum, Source Address, Destination Address, Options.
    -   **IPv4 Header Options:** Security, Strict Source Routing, Loose Source Routing, Record Route, Timestamp.
-   **Prefixes:** 32-bit address with variable-length network portion and host portion. Written in dotted decimal notation (e.g., `128.208.2.151`). Network address with prefix length (e.g., `128.208.2.0/24` - CIDR notation).
    -   **Subnets:** Splitting a block of addresses into several internal networks while appearing as a single network externally. (Example of subnetting a /16 block).
-   **Classless InterDomain Routing (CIDR):** Allows route aggregation (combining small prefixes into larger ones) to reduce routing table size. (Example of IP block allocation using CIDR).
-   **Classful and Special Addressing (Historical):**
    -   Class A, B, C, D (Multicast), E (Reserved). Classful system wasted many addresses. Bits for class A, B, C no longer used this way.
    -   **Special Addresses:** `0.0.0.0` (this host), `255.255.255.255` (broadcast on local network), `127.x.y.z` (loopback).
-   **Network Address Translation (NAT):** Short-term solution for IPv4 address exhaustion.
    -   Assigns a single public IP to a home/business; internal devices use private IPs. Translation occurs at the customer network boundary.
    -   Uses private IP ranges (`10.0.0.0/8`, `172.16.0.0/12`, `192.168.0.0/16`).
    -   Complications: Breaks end-to-end model, makes Internet somewhat connection-oriented at NAT device, violates protocol layering.
-   **IP Version 6 (IPv6):**
    -   **Header Fields:** Version, Differentiated Services, Flow Label, Payload Length, Next Header, Hop Limit, Source Address (128 bits), Destination Address (128 bits).
    -   **Header Fields Removed from IPv4:** IHL, Protocol, Fragmentation fields, Checksum.
    -   **Extension Headers (Optional):** Hop-by-hop options, Destination options, Routing, Fragmentation, Authentication, Encrypted security payload. Each has a "Next Header" field.
-   **Internet Control Message Protocol (ICMP):**
    -   Used by routers to report unexpected events during packet processing to the sender.
    -   **Important Message Types:** Destination Unreachable, Time Exceeded, Parameter Problem, Source Quench, Redirect, Echo/Echo Reply, Timestamp Request/Reply, Router Advertisement/Solicitation.
-   **Address Resolution Protocol (ARP):**
    -   Maps IP addresses to Data Link Layer addresses (e.g., Ethernet MAC addresses).
    -   NICs have unique 48-bit Ethernet addresses.
    -   (Example of ARP process for local and remote communication).
-   **Dynamic Host Configuration Protocol (DHCP):**
    -   Automatically assigns IP addresses and network configuration (gateway, mask, DNS) to hosts.
    -   Requires a DHCP server; IPs leased from a pool.
-   **MultiProtocol Label Switching (MPLS):**
    -   Allows connection-oriented services over IP networks, used for VPNs.
    -   Adds a label to packets; forwarding based on label. Operates between Layer 2 and Layer 3.
    -   **MPLS Header:** Label (20 bits), QoS (3 bits), S (1 bit - stack), TtL (8 bits).
    -   **Components:** Label Edge Router (LER - adds/removes labels), Label Switch Router (LSR - switches based on labels).

### Routing Protocols:
-   **Open Shortest Path First (OSPF):** An intradomain routing protocol (Interior Gateway Protocol - IGP).
    -   Abstracts network into a directed graph with weighted arcs. Point-to-point links are two arcs; broadcast networks represented by a network node.
    -   Supports areas, with Area 0 as backbone. Routers can be area border, backbone, AS boundary, or internal.
    -   **Message Types:** Hello, Link State Update, Link State Ack, Database Description, Link State Request.
    -   Supports Equal Cost MultiPath (ECMP) for load balancing.
-   **Border Gateway Protocol (BGP):** An interdomain routing protocol (Exterior Gateway Protocol - EGP).
    -   Deals with routing policies between ASes (e.g., not carrying transit traffic for others, avoiding certain routes).
    -   Path vector protocol: keeps track of the AS path used, not just cost.
    -   Route advertisements propagate AS paths.
    -   **Routing Policies:** Transit, Customer, Peer.
    -   **Peering:** ASes agree to exchange traffic directly.
    -   **Stub Network:** Connected via a single link, doesn't need BGP.
    -   **Multihoming:** Connecting to multiple ISPs for reliability.
    -   **iBGP (internal BGP):** Used to propagate BGP routes within an AS.
    -   **eBGP (external BGP):** Regular BGP between ASes. (Diagram showing iBGP and eBGP).
-   **Internet Multicasting:**
    -   One-to-many communication using Class D IP addresses (e.g., streaming live events).
    -   `224.0.0.0/24` reserved for local network multicast (no routing protocol needed, routers don't forward off LAN).
    -   Examples: `224.0.0.1` (all systems on LAN), `224.0.0.2` (all routers on LAN).
-   **Internet Group Management Protocol (IGMP):** Used by hosts and routers to communicate group memberships.
-   **Multicast Routing Protocols (build spanning trees):**
    -   **PIM (Protocol Independent Multicast):**
        -   **Dense Mode:** For widespread members (e.g., data center file distribution).
        -   **Sparse Mode:** For scattered members (e.g., IPTV).
        -   **Source-Specific Multicast:** Optimized for single sender.
    -   BGP extensions or tunnels for inter-AS multicast.

## Topic 5: Transport Layer

This chapter details how end-to-end communication and reliable data transfer are achieved between processes on different hosts.

### Transport Layer Overview:
-   Provides data transport from a process on a source machine to a process on a destination machine.
-   Offers reliability independent of the physical network.
-   Network layer enables end-to-end packet delivery; transport layer builds on this for process-to-process delivery.
-   **Transport Layer Services:**
    -   **Services Provided to Upper Layers:** Efficient, reliable, cost-effective data transmission for application layer processes.
    -   Obtains services from the Network layer.
-   **Transport Entity:** Software/hardware performing transport tasks (in OS kernel, library package, or NIC). (Visual diagram of entities).
-   **Types of Transport Services:**
    -   **Connection-Oriented:** Three phases: Connection establishment, Data transfer, Release.
    -   **Connectionless.**
-   **Need for Transport Layer (even if network service is similar):**
    -   Transport services execute on users' machines; network services mainly on routers.
    -   Users have no control over network devices; transport layer provides improved quality of service.
    -   Can make transport service more reliable than underlying network.
    -   Provides standard primitives for application programmers.
-   **Transport Layer Primitives:**
    -   **Difference from Network Services:** Network layer works with real networks (unreliable); connection-oriented transport service aims to be reliable on top of this. Hides network imperfections. Can also provide unreliable service (e.g., video streaming).
    -   Transport primitives are used by many application programs.
-   **Simple Transport Service Primitives:** `LISTEN`, `CONNECT`, `SEND`, `RECEIVE`, `DISCONNECT`.
    -   **Connection Establishment:** Server `LISTEN`s, client `CONNECT`s (sends `CONNECTION REQUEST`). Server accepts (sends `CONNECTION ACCEPTED`). Data exchanged via `SEND`/`RECEIVE`.
    -   **Disconnection:** Asymmetric (either user disconnects) or Symmetric (both users must issue `DISCONNECT`). (State diagram of primitives).

### Internet Transport Protocols:
-   **UDP (User Datagram Protocol):** Connectionless.
-   **TCP (Transmission Control Protocol):** Connection-oriented.

### User Datagram Protocol (UDP):
-   Allows applications to send encapsulated IP datagrams without establishing a connection.
-   **UDP Header (8 bytes):** Source Port, Destination Port, UDP Length, UDP Checksum.
    -   **Ports:** Identify the application process.
    -   **UDP Length:** Total segment length (header + data), min 8 bytes, max 65,515 bytes.
    -   **UDP Checksum:** For reliability; covers header, data, and an IP pseudo-header. (IPv4 pseudo-header format).
-   **Remote Procedure Call (RPC) using UDP:**
    -   Allows a procedure on one machine (client) to call a procedure on another machine (server).
    -   **Stubs:** Client stub (represents server procedure locally) and Server stub (represents client procedure locally) hide non-local nature.
    -   **RPC Steps:**
        1.  Client calls client stub (local call, parameters on stack).
        2.  Client stub marshals parameters into a message, makes system call to send.
        3.  OS sends message client to server.
        4.  Server OS passes packet to server stub.
        5.  Server stub unmarshals parameters, calls server procedure. Reply follows same path.
    -   **Problems in RPC:** Pointer parameters, variable parameter sizes, deducing parameter types, global variable access.
-   **Real-Time Transport Protocol (RTP) using UDP:**
    -   Transports audio/video packets and ensures timely playout. (Packet nesting diagram: RTP in UDP in IP in Ethernet).
    -   Multiplexes real-time data streams onto UDP.
    -   No delivery guarantees (UDP properties).
    -   Packets numbered sequentially to detect loss (application handles, no retransmission by RTP).
    -   Timestamp: For buffering at destination and synchronization.
    -   **RTP Header:** Version, P, X, CC, M, Payload Type, Sequence Number, Timestamp, Synchronization Source Identifier, Contributing Source Identifier(s).
-   **Real-Time Transport Control Protocol (RTCP):**
    -   Provides feedback on delay, jitter, bandwidth, congestion to sources.
    -   Allows encoding algorithms to adapt for best quality.
-   **Playout with Buffering and Jitter Control:** Buffering at receiver to handle jitter (variation in packet arrival delay). (Diagram showing buffering).
    -   If packets too delayed: skip or stop playback. Playback point depends on jitter.

### Transmission Control Protocol (TCP):
-   Provides reliable end-to-end byte stream over unreliable internetwork.
-   Adapts to varying network properties (topology, bandwidth, delay).
-   TCP entity (kernel, library, process) breaks user data into segments (<64KB), sends as IP datagrams, reconstructs at receiver.
-   Connections are full-duplex and point-to-point.
-   **TCP Service Model:**
    -   Uses Sockets as endpoints. Socket number = IP address + 16-bit Port.
    -   Connection explicitly established between sockets.
    -   **Ports:** Below 1024 reserved for standard services (well-known ports, e.g., FTP 20/21, SSH 22, HTTP 80, HTTPS 443).
-   **The TCP Protocol:**
    -   Each byte has a 32-bit sequence number.
    -   Data exchanged in segments (fixed 20-byte header + options + data).
    -   Segment size decided by TCP software, limited by IP payload (65,515 bytes) and link MTU.
    -   Sender starts timer; if ACK not received before timeout, retransmits. Receiver ACKs with next expected sequence number.
    -   Cannot ACK segment B if segment A (expected before B) hasn't arrived.
-   **TCP Segment Header:**
    -   Source Port, Destination Port (identifies connection endpoints with IP).
    -   Sequence Number, Acknowledgment Number.
    -   TCP Header Length (number of 32-bit words, due to variable Options field).
    -   **Flags (1-bit):**
        -   `CWR`, `ECE`: Congestion signaling.
        -   `URG`: Urgent data.
        -   `ACK`: Acknowledgement segment.
        -   `PSH`: Push data immediately to application.
        -   `RST`: Reset connection due to problem.
        -   `SYN`: Synchronize sequence numbers (connection establishment).
        -   `FIN`: Finish, no more data from sender (connection termination).
    -   Window Size: Bytes sender may send.
    -   Checksum.
    -   Urgent Pointer: Offset for urgent data.
    -   Options: Extra facilities.
-   **TCP Connection Establishment (Three-Way Handshake):**
    1.  Client sends `CONNECT` (`SYN=1`, `ACK=0`, `Seq=x`) to Server (LISTENing).
    2.  Server, if accepting, sends (`SYN=1`, `ACK=1`, `Seq=y`, `Ack=x+1`). If not, sends `RST`.
    3.  Client sends (`ACK=1`, `Seq=x+1`, `Ack=y+1`).
    -   (Diagram of handshake).
-   **TCP Connection Release:**
    1.  Party A sends `FIN`.
    2.  Party B acknowledges `FIN` (that direction closed for new data from A). Data can still flow from B to A.
    3.  Party B sends `FIN`.
    4.  Party A acknowledges `FIN`. Both directions closed.
    -   (Requires four segments: `FIN` and `ACK` in each direction).
-   **TCP Connection Management Modeling (Finite State Machine):** States include CLOSED, LISTEN, SYN RCVD, SYN SENT, ESTABLISHED, FIN WAIT 1, FIN WAIT 2, TIME WAIT, CLOSING, CLOSE WAIT, LAST ACK. (State transition diagram).
-   **TCP Sliding Window (Flow Control):**
    -   Receiver advertises window size (available buffer space). Sender sends up to this amount.
    -   If window is 0, sender stops unless urgent data or sending a 1-byte segment (window probe) to force re-announcement.
    -   **Delayed Acknowledgements:** Delay ACKs/window updates (up to 500ms) to reduce short packets.
    -   **Nagle's Algorithm:** Send first small piece, buffer rest until ACKed, then send all buffered data.
    -   **Silly Window Syndrome:** Receiver reads 1 byte at a time, advertising tiny windows. Solution: Receiver doesn't update window until substantial space available.
    -   Handling out-of-order segments: Buffer until they can be passed to application in order.
    -   **Cumulative Acknowledgement:** ACKs up to the byte received contiguously. If segments 0-3, 5-7 received, ACKs up to 3. When 4 arrives, can ACK up to 7.
-   **TCP Congestion Control:**
    -   Handles network overload using a congestion window and packet loss as a signal.
    -   Congestion window: Bytes sender may have in network. Rate = window / RTT.
    -   Works with flow control window; TCP stops if either is full.
    -   Packet loss is primary congestion signal. Transmission errors less common cause due to link-layer retransmissions (e.g., 802.11) and low error rates on wired media.
    -   **ACK clocking:** ACKs return at rate of slowest link, pacing sender.
    -   **Slow Start Algorithm:** Congestion window (`cwnd`) starts at 1 packet, doubles each RTT (1, 2, 4, 8...).
    -   When packet loss occurs, threshold is set (e.g., half of current `cwnd`), and slow start restarts. If `cwnd` reaches threshold, switches to additive increase (congestion avoidance).
    -   **Fast Recovery:** Instead of full slow start after loss, set `cwnd` to new threshold (or half previous `cwnd`) and continue with additive increase (sawtooth pattern).

## Topic 6: Application Networking Services

This chapter explores common application layer protocols that users interact with.

### Application Layer Overview:
-   Provides services for user applications, building on transport layer services.
-   **Protocols:** DNS, SMTP, IMAP, WWW.

### Domain Name System (DNS):
-   Maps human-readable names (e.g., `google.com`) to IP addresses (e.g., `173.194.210.113`).
-   Replaced earlier `host.txt` file system due to scale.
-   Hierarchical, domain-based naming scheme using a distributed database.
-   **Resolution Process:** Application calls resolver -> resolver queries local DNS server -> server looks up/queries others and returns IP -> resolver returns IP to app. Queries/responses typically UDP.
-   **DNS Name Space:**
    -   Managed by ICANN. Internet divided into ~250 top-level domains (TLDs). Domains partitioned into subdomains, forming a tree structure.
-   **Top-Level Domains (TLDs):**
    -   **Generic (gTLDs):** `.com`, `.edu`, `.gov`, `.org`, `.net`, `.biz`, `.info`, etc.
    -   **Country Code (ccTLDs):** One for each country (e.g., `.uk`, `.jp`, `.us`).
-   **Obtaining a second-level domain:** Contact registrar for the TLD, check availability, pay fee.
-   **Cybersquatting:** Registering domains to sell at higher prices.
-   Domain names formed by path to root, components separated by periods, case-insensitive.
-   **Domain Resource Records (RRs):** DNS database entries.
    -   Tuple: (Domain name, Time to live, Class, Type, Value).
    -   **Types:** `SOA` (Start of Authority), `A` (IPv4 address), `AAAA` (IPv6 address), `MX` (Mail Exchange), `NS` (Name Server), `CNAME` (Canonical Name), `PTR` (Pointer), `SPF`, `SRV`, `TXT`.
-   **Name Servers:**
    -   DNS namespace divided into non-overlapping zones. Each zone has one or more Name Servers.
    -   **Primary Name Server:** Gets info from local disk file.
    -   **Secondary Name Server(s):** Get info from primary; some may be outside zone for reliability.
-   **Name Resolution:** Resolver queries local name server. If not cached, local server starts remote query (e.g., to root server, then TLD server, then authoritative server). (Example resolution steps).

### Electronic Mail (Email):
-   **Architecture and Services:**
    -   **User Agent (UA):** Allows users to read/send email (GUI or text-based). Manages mailboxes, composes, replies, filters.
    -   **Message Transfer Agents (MTAs / Mail Servers):** Move messages source to destination using SMTP. System processes running in background. Handle mailing lists. Advanced features: CC, BCC, priority, encryption.
    -   **Mailboxes:** Store received email, maintained by mail servers. UAs present view of mailbox.
-   **Message Format:**
    -   **Envelope:** Encapsulates message, contains transport info (destination address, priority, security).
    -   **Header:** Control information for UAs.
    -   **Body:** User-created message content.
    -   (Analogy to paper mail).
-   **User Agents (Email Readers):** Examples: Gmail, Outlook, Thunderbird, Apple Mail.
    -   Interface elements: Message folders, summary, search.
    -   Features: GUI, message summary (icons for attachments, unread, important), folders, message disposition (delete, reply, forward, keep).
    -   Spam filtering, auto-responders, signature blocks.
-   **SMTP (Simple Mail Transfer Protocol):**
    -   Simple ASCII protocol, uses TCP port 25.
    -   Client establishes TCP connection with SMTP server. Server accepts connections and messages.
    -   Error reports returned if undeliverable.
    -   Server speaks first after connection.
    -   **Commands:** `HELO` (or `EHLO` for ESMTP), `MAIL FROM`, `RCPT TO`, `DATA`, `QUIT`. Multiple recipients allowed.
    -   **ESMTP Extensions:** `AUTH` (authentication), `BINARYMIME`, `CHUNKING`, `SIZE`, `STARTTLS`, `UTF8SMTP`.
-   **Mail Submission:** SMTP with `AUTH` extension used for client to submit mail to their sending mail server.
-   **Mail Transfer:** Sending MTA delivers to receiving MTA using SMTP.
-   (Diagram of mail flow: Sending UA -> Sending Mail Server (SMTP) -> Receiving Mail Server (SMTP) -> Receiving UA (POP/IMAP)).
-   **IMAP (Internet Message Access Protocol):**
    -   Server listens on TCP port 143. Client connects and issues commands.
    -   Allows fetching messages, marking with flags, organizing into folders on the server.
    -   **Commands:** `CAPABILITY`, `STARTTLS`, `LOGIN`, `AUTHENTICATE`, `SELECT`, `EXAMINE`, `CREATE`, `DELETE`, `RENAME`, `SUBSCRIBE`, `LIST`, `STATUS`, `APPEND`, `FETCH`, `SEARCH`, `STORE`, `COPY`, `EXPUNGE`, `CLOSE`, `LOGOUT`.

### World Wide Web (WWW):
-   Vast collection of content as Web pages, linked via hyperlinks.
-   Viewed by browsers (Chrome, Firefox, Safari, Edge).
-   **Architecture:**
    -   Browser displays page on client. Page fetched by sending requests to server(s).
    -   **HTTP (HyperText Transfer Protocol):** Used for request/response.
-   **Page Types:**
    -   **Static Pages:** Same content each time.
    -   **Dynamic Pages:** Generated on demand or contain programs.
-   Content from different servers integrated by browser (text, graphics, video).
-   **Client Side:**
    -   **URL (Uniform Resource Locator):** Worldwide name for a page. Parts: Protocol (`http`), DNS name (`www.bit.lk`), Path (`index.html`).
    -   **Browser Steps (when clicking a link):**
        1.  Determine URL.
        2.  Ask DNS for IP address.
        3.  DNS replies with IP.
        4.  Browser makes TCP connection to IP on port 80 (for HTTP).
        5.  Sends HTTP request for page.
        6.  Server sends page as HTTP response.
        7.  If page includes other URLs (images, videos, scripts), browser fetches them similarly.
        8.  Browser displays page.
        9.  TCP connections released after short period if no more requests.
    -   **Common URL Schemes:** `http`, `https`, `ftp`, `file`, `mailto`, `rtsp`, `sip`, `about`.
-   **Handling Rich Content (MPEG, PDF, JPEG):**
    -   Server returns page with MIME (Multipurpose Internet Mail Extensions) type.
    -   Browser uses MIME type to determine display method: Plug-ins or Helper applications. (Diagram of plug-ins vs. helpers).
    -   **MIME Types:** `text` (plain, html), `image` (gif, jpeg), `audio` (mpeg), `video` (mpeg), `application` (pdf, javascript), etc.
-   **Server Side Actions:**
    1.  Accept TCP connection from client.
    2.  Get path to requested file/page.
    3.  Get file (from disk).
    4.  Send file contents to client.
    5.  Release TCP connection.
-   **Cookies:** Small, named strings server associates with a browser. Not executable.
    -   Fields: Domain, Path, Content, Expires, Secure.
    -   Browser checks cookie directory before sending request; includes relevant cookies from that domain.
    -   Server interprets cookies (identify customer, shopping cart, tracking).

## Topic 7: Network Management

This chapter covers security mechanisms like firewalls and VPNs, and the broader aspects of managing networks.

### Firewalls:
-   Perimeter protection device; all traffic entering/leaving passes through it.
-   Filters traffic based on rules. (Diagram showing firewall placement with DMZ).
-   **Packet Filter:** Uses whitelisting (block all, allow specific) or blacklisting (allow all, block specific).
-   **Filtering criteria:** Source/Destination IP, Source/Destination Port. Ports indicate service (TCP 25 for mail, TCP 80 for HTTP).
-   **DMZ (DeMilitarized Zone):** Area outside the security perimeter for publicly accessible servers (web, email). Internal access to DMZ servers can have specific rules.
-   **Stateful Firewalls:** Track connections, not just individual packets. Allows more effective rules (e.g., allow HTTP response only if request originated internally).
-   **Application-Level Gateways:** Inspect application-level protocols. Can distinguish Web Browse HTTP from P2P HTTP, prevent sensitive email exfiltration.
-   **Limitations:** Can be bypassed by spoofed source addresses, single defense perimeter, may not stop all DoS/DDoS attacks.

### Virtual Private Networks (VPNs):
-   **Private Network:** Built from company computers and leased lines; secure but expensive and not scalable.
-   **VPN:** Overlay network on public networks with private network properties. Examples: MPLS (ISP-provided), IPSec (company-implemented).

### Network Management Requirements:
-   Essential as networks grow in complexity and importance.
-   Need for automated tools that can:
    -   Communicate with multi-vendor devices.
    -   Centralize coordination (monitoring, updates).
-   **ISO Network Management Framework (FCAPS):**
    -   Fault Management
    -   Accounting Management
    -   Configuration Management
    -   Performance Management
    -   Security Management

### Fault Management:
-   Detecting, isolating, and correcting abnormal operations. Includes maintaining error logs, tracing faults, diagnostic tests.
-   Distinguish faults from occasional errors (e.g., CRC errors vs. excessive errors indicating a fault).
-   **User Expectations:** Reliable problem resolution, consistent quality service, immediate correction, informed of status and resumption times.
-   **NMS Functional Requirements:**
    -   **Detecting/Reporting:** Log events/errors, monitor, identify faults, generate reports, send notifications.
    -   **Diagnosis:** Activate diagnostics, request fault data, analyze data, exchange info.
    -   **Correction:** Change attributes, take components down/up, reconfigure, track operations post-correction.
    -   **Robustness:** Redundant fault manager systems.

### Accounting Management:
-   Establishing charges for resource use, identifying costs. Informing users of costs, setting limits, combining costs for multiple resources.
-   **User Expectations:** Specify info to record, interval, algorithms. Authorized access to accounting info.
-   **NMS Functional Requirements:**
    -   **Recording/Generating Info:** Specify info to collect, duration. Mechanisms to record/collect and generate messages.
    -   **Controlling Storage/Access:** Standard procedures to retrieve/store; limited access.
    -   **Reporting Info:** Report usage/charges. Transmit accounting news (rate changes).
    -   **Setting/Modifying Limits:** Read, set, change limits for user groups. Change priorities.
    -   **Defining Metrics:** Time, speed, storage capacity, etc.

### Configuration Management:
-   Identifying, controlling, collecting data from, and providing data to open systems for operation. Setting parameters, naming objects, initializing/closing objects, collecting/announcing status changes, changing configuration.
-   **User Expectations:** Start/shutdown devices, define connectivity, set/modify/load/export configurations, informed of status (software versions, patches).
-   **NMS Functional Requirements:**
    -   **Defining Resources/Attributes:** Specify resources, attributes, value ranges.
    -   **Setting/Modifying Attribute Values:** Set/modify values (e.g., activate ports), load defaults.
    -   **Defining/Modifying Relationships:** Specify relationships (topology, hierarchy, connection, management domain). Add, delete, modify.
    -   **Examining Values/Relationships:** Examine attributes/values. Track changes.
    -   **Distributing Software:** Examine, update, manage software versions/routing info.
    -   **Initializing/Terminating Operations:** Start/close network/subnetwork operations.
    -   **Verifying Authorization:** Only authorized users perform config functions.
    -   **Reporting Status:** Notify of config changes. Request/obtain config reports.

### Performance Management:
-   Evaluating resource behavior and communication effectiveness. Gathering stats, maintaining logs, determining performance, altering modes for testing.
-   Deals with quality and effectiveness (error levels, responsiveness, availability, utilization).
-   **Categories:**
    -   **Monitoring:** Tracking network activities. Identify resources, associate metrics/values.
    -   **Tuning:** Making adjustments to improve performance (setting traffic parameters, allocating resources, fault management if severe).
-   **User Expectations:** Info on response times, reliability, availability. Managers need stats for planning. Adequate capacity.
-   **NMS Functional Requirements:**
    -   **Monitoring:** Select items to monitor, start/stop times, frequency, thresholds for alerts.
    -   **Tuning/Controlling:** Execute tests, collect results, change allocation/attributes.
    -   **Evaluating Tuning:** Track results against criteria.
    -   **Reporting:** Notify of abnormal changes. Request/obtain reports. Display snapshots, statistics (avg, max, min).
    -   **Testing Capacity:** Run tests for loading under natural/artificial conditions.

### Security Management:
-   Supporting security policies: creating/deleting/controlling security services/mechanisms, distributing security info, reporting security events.
-   **Management Activities:**
    -   **Administration:** Gathering and managing security management info.
    -   **Detection:** Auditing security operations (audit trail specification, analysis, reporting, archiving).
    -   **Recovery:** Recovering from attacks.
-   **OSI Security Goals:** Authentication, Access Control, Confidentiality, Integrity, Non-repudiation.
-   **NMS Functional Requirements:**
    -   **Controlling Access:** Grant/restrict access to network/parts for users/roles.
    -   **Archiving/Retrieving Info:** Gather, store, access info for analysis/control.
    -   **Managing Encryption:** Encrypt communications, key management.

### Simple Network Management Protocol (SNMP):
-   For querying network devices for state (data rates, CPU load, errors) and setting parameters.
-   Supported by most modern devices.
-   **Communication:** UDP port 161 (Manager to Agent), UDP port 162 (Agent Traps to Manager).
-   **Protocol Data Units (PDUs):** Messages between Manager and Agent.
    -   `GETREQUEST`, `GETNEXTREQUEST`, `SETREQUEST` (Manager to Agent).
    -   `RESPONSE` (Agent to Manager).
    -   `GETBULKREQUEST` (Manager to Agent).
    -   `INFORMREQUEST` (Manager/Agent to Manager, acknowledged).
    -   `TRAP` (Agent to Manager, unacknowledged asynchronous notification).
-   **Management Information Base (MIB):** Database of device variables/parameters (CPU load, vendor name) maintained by Agent.
    -   Manager uses MIB to query device and translate info.
    -   Managed objects identified by globally unique Object Identifier (OID), hierarchical tree structure. (Example OID tree and specific OIDs).
-   **SNMP Architecture:** Manager, Agent, MIB. (Diagram for v1. Diagram for v2c with Mid-Level Manager).
-   **Communication Types:**
    -   **Asynchronous:** `TRAP` (unacknowledged), `INFORMREQUEST` (acknowledged).
    -   **Synchronous:** Poll (retrieving MIB variables at intervals).
-   **SNMP Versions:**
    -   `v1`, `v2c` are insecure.
    -   `v3` uses user-based authentication and supports encrypted messages (DES, Triple DES, AES).

## Topic 8: Software Defined Networks (SDN)

This chapter introduces the concepts and architecture of Software Defined Networks.

### Modern Data Center:
-   Hosts complex web services. Warehouses for servers with environmental protection, redundant power, duplicate capacity at different locations.
-   Servers arranged in rows of racks. Typical topology: Core switch -> Aggregation switch -> Top-of-Rack (ToR) switch -> Servers.

### Traditional Switch Architecture (Planes):
-   (Diagram of planes).
-   **Data Plane:** Ports for packet reception/transmission. Handles packet buffering, scheduling, header modification, forwarding based on forwarding table. If info not in table or control packet, passes to control plane.
-   **Control Plane:** Updates forwarding table for data plane. Processes control protocols that manage network topology. Requires general-purpose microprocessors and software.
-   **Management Plane:** Used by administrators to configure/monitor the network. Extracts/modifies data in control/data planes via network management systems.

### Evolution of Switches and Control Planes:
-   **Simple Forwarding and Routing using Software:** Early days, most functions in software. Over time, basic functions moved to hardware. (Diagram showing evolution from ~1990 to ~2005).
-   **Hardware Forwarding and Control in Software:** Layer 2 (MAC forwarding) and Layer 3 (routing) forwarding in hardware tables. ACLs also in hardware. Control (broader routing, topology convergence) in software on device.
-   **Moving Control Off of the Device (SDN Concept):** Control software (intelligence for paths, outages, demands) moved from device to a central controller with a global network view.
    -   Forwarding/Filtering/Prioritization remains on device (hardware tables).
    -   Control software centralized.
    -   Applications run above controller.

### Overview of SDN Architecture:
-   **Fundamental Characteristics:**
    -   **Plane Separation:** Forwarding and control planes separated.
    -   **Simplified Device & Centralized Control:** Devices simpler as control is centralized.
    -   **Network Automation & Virtualization:**
        -   Distributed state abstraction (global network view).
        -   Forwarding abstraction (specify behavior without vendor hardware knowledge).
        -   Configuration abstraction (define goals without implementation details).
    -   **Openness:** Standard, well-documented, not proprietary.
-   Centralized controller provides open interface for automated control.
-   **Open SDN APIs:**
    -   **Northbound API:** Allows applications to plug into controller to provide algorithms/protocols.
    -   **Southbound API (e.g., OpenFlow):** Controller uses to program network devices.
-   **Main Components of SDN:**
    -   **SDN Devices:** API for controller communication, abstraction layer, packet processing function. (Anatomy of software switch and hardware switch).
    -   **SDN Controller:** Maintains network view, implements policies, controls devices, provides northbound API. (Controller anatomy diagram).
    -   **SDN Applications:** Run above controller, interface via northbound API.

### Introduction to OpenFlow:
-   A key SDN technology.
-   Defines communication protocol between SDN data plane and control plane.
-   Does not describe controller behavior itself.
-   **System:** OpenFlow controller communicates with OpenFlow Switches. Protocol defines messages/formats; behavior specifies device reactions and responses to controller.

### SDN Use Case - Data Center Orchestration:
-   Implementation still evolving. Some orgs use Open SDN or Overlays.
-   Examples: Google (OpenFlow for WAN, moving to data centers), Microsoft Azure (Overlay with NVGRE, enhanced OpenFlow), Ebay (VMware Nicira for public cloud).
-   Early attempts at SDN: RADIUS (Server and Network Policy updates attributes on switches), Orchestration (scripts update devices via vendor plugins using SNMP/CLI).
