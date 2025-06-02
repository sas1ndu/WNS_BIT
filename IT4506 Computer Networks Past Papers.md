## Summary of IT4506 Computer Networks Past Papers (2021, 2022, 2023)

The IT4506 Computer Networks examination consistently follows a two-part structure:

### Part 1: Multiple Choice Questions (MCQ)
-   This section contains 25 MCQ questions.
-   Each question offers 5 choices with **only one correct answer**.
-   All questions must be answered.
-   The duration for Part 1 is typically **one hour** (though the 2023 paper indicates 2 hours for both parts combined).
-   Answers are marked on a special machine-readable answer sheet.
-   Calculators are generally **not allowed** (2023, 2021) or non-programmable calculators may be used (2022).
-   Electronic devices capable of storing/retrieving text are **not allowed**.

---
### Part 2: Structured Questions
-   This section typically contains 2 structured questions.
-   Students are required to answer **both questions**.
-   Answers are to be written in the space provided on the question paper.
-   The duration for Part 2 is usually **one hour** (though the 2023 paper indicates 2 hours for both parts combined).

The final mark for the paper is an average of the scores from Part 1 and Part 2, each graded out of 100.

---
## Content Analysis & Recurring Themes:

Based on the questions from the provided past papers, the IT4506 course emphasizes a broad understanding of networking concepts, from physical transmission to application services and modern network architectures.

### Key Content Areas Frequently Tested:

-   **OSI Model and Protocol Data Units (PDUs):**
    -   Identifying layers responsible for specific functions (e.g., process-to-process delivery - **Transport Layer**).
    -   Knowing the **PDU names** for different layers (e.g., Segment for Transport Layer, Frame for Data Link Layer, Packet for Network Layer).
    -   Understanding the hierarchy and encapsulation of PDUs.

-   **Transmission Media and Physical Layer Concepts:**
    -   Comparing bandwidth of different media (**Twisted Pair < Coaxial Cable < Fiber Optic Cable**).
    -   Understanding concepts like **Hamming distance** for error detection.
    -   Calculating maximum data rates (**Nyquist theorem** for noiseless channels).
    -   Properties of electromagnetic waves (wavelength, frequency).
    -   Purpose of physical characteristics of media (e.g., twists in twisted pair cables).

-   **Data Link Layer:**
    -   **MAC sublayer's** role and its position within the OSI model.
    -   Framing techniques like **byte stuffing**.
    -   Protocols used in LANs (**Ethernet, IEEE 802.11**).
    -   **Ethernet Preamble** content and purpose.
    -   Issues with redundant links (loops) and mitigation methods (**Spanning Tree Protocol**).
    -   **MAC addresses** and their role in forwarding.
    -   **CSMA persistence methods** (p-persistent CSMA).
    -   **Cut-through switching**.

-   **Network Layer and IP Addressing:**
    -   **IP Addressing (IPv4):**
        -   **Subnet masks** (dotted decimal and CIDR notation).
        -   Calculating the maximum number of hosts in a subnet.
        -   Determining **broadcast addresses**.
        -   **Subnetting** and calculating network addresses of subnetworks.
        -   Identifying **default gateways**.
    -   Destination IP address in packet forwarding.
    -   **Protocols:**
        -   **ARP (Address Resolution Protocol)** for MAC address discovery.
        -   **DHCP (Dynamic Host Configuration Protocol)** for IP configuration, including DISCOVER messages and broadcast MAC addresses.
    -   Role of routers in connecting different LANs and forwarding IP datagrams.
    -   Understanding that IP headers (and thus frames carrying them) do not inherently contain subnet mask information.
    -   **IP packet fragmentation** if frame sizes differ across networks.
    -   Source IP address remains unchanged as a packet traverses routers.

-   **Transport Layer:**
    -   **TCP (Transmission Control Protocol):**
        -   Fixed header size (20 bytes).
        -   Flags (e.g., **PSH** for immediate sending).
        -   Port numbers (valid ranges, recognizing non-valid ports).
        -   Checksum field range.
        -   Congestion control (threshold adjustment after packet loss).
        -   Retransmission on timer expiry.
        -   **RST flag** for terminating problematic connections.
        -   Protocol used for web requests (TCP).
    -   **UDP (User Datagram Protocol):**
        -   Header fields (Source Port, Destination Port, Length, Checksum; MAC address is NOT part of UDP header).
        -   Underlying protocol for RTP.
    -   Main objective: efficient, reliable, cost-effective data transmission for application processes.
    -   Location of the Transport Entity (kernel, library, NIC).
    -   Purpose of port numbers: uniquely identify applications/processes on a host.

-   **Application Layer:**
    -   **DNS (Domain Name System):**
        -   **Resource Record types** (e.g., MX for mail servers, A for IPv4 addresses).
        -   Mapping a domain name to multiple IP addresses (using multiple A records).
        -   Historical context (hosts.txt in ARPANET).
    -   **HTTP (HyperText Transfer Protocol):** Protocol used by PCO for web requests.
    -   **Email Architecture:**
        -   Components: Sender/Receiver User Agent, Message Transfer Agent, Mailbox.
        -   Protocols: **SMTP** (and ESMTP extensions like AUTH, BINARYMIME).
    -   **RPC (Remote Procedure Call):**
        -   **Marshalling** (packing parameters).
        -   Steps involved (e.g., OS passing packet to server stub).
        -   Client stub representing server procedure in client's address space.
    -   **RTP (Real-Time Transport Protocol):** Placement in protocol stack (User Space, above Socket Interface).
    -   Identifying Application Layer protocols (e.g., TCP is Transport, not Application).
    -   Standard port numbers (e.g., SSH on port 22).

-   **Network Management & Security:**
    -   Purpose of **VPNs** (secure/private communication over Internet).
    -   **ISO Network Management Functional Areas** (Fault, Security, Performance, Configuration, but NOT Infrastructure management as a distinct top-level area).
    -   Limitations of private networks built with leased lines (e.g., Scalability).

-   **Software Defined Networks (SDN):**
    -   Role of **Northbound/Southbound APIs** (Southbound for controller to program switches).
    -   Fundamental concept: decoupling forwarding and control functions.
    -   **SDN Controller:** Maintains network view, implements policy decisions.
    -   Traditional Switch Architecture planes (Data plane for packet buffering/scheduling).
    -   Advantages of hardware routing tables (speed).

---
### General Observations:

-   The exams cover a mix of theoretical knowledge (OSI layers, protocol functions) and practical application (IP addressing, subnetting, interpreting network diagrams).
-   Network diagrams are frequently used as a basis for multiple questions, requiring students to trace packet flows and identify relevant protocols and addresses at different points.
-   Understanding the distinction and interaction between different layers of the OSI or TCP/IP model is crucial.
-   Specific details of common protocols like TCP, UDP, IP, Ethernet, DNS, SMTP, and HTTP are regularly tested.
-   Newer concepts like SDN are also included, focusing on architecture and key components.

This summary should provide a good overview of what to expect from the IT4506 Computer Networks exam.
