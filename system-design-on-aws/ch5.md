# Chapter 5. Communication Networks and Protocols

## Communication Models

### Open Systems Interconnection (OSI)

- divide the communication process into 7  layers
- each layer is responsible for a specific task
- Layers
  - Layer 7: Application
    - HTTP, SMTP, FTP, DNS
  - Layer 6: Presentation
    - Data encryption, data compression
  - Layer 5: Session
    - Establish, manage, and terminate connections between applications
    - Session layer protocols
      - NetBIOS, PPTP, RPC, SCP, SMB, SSH, Telnet
  - Layer 4: Transport
    - TCP, UDP
    - Data segmentation, error detection, and correction
  - Layer 3: Network
    - IP, ICMP, IGMP, ARP, RARP
    - Routing, addressing, and packet forwarding
  - Layer 2: Data Link
    - Ethernet, PPP, Frame Relay, ATM
    - Data framing, error detection, and MAC addressing
  - Layer 1: Physical
    - Ethernet, Wi-Fi, Bluetooth, DSL, ISDN
    - Physical media, signal encoding, and transmission

### Transmission Control Protocol/Internet Protocol (TCP/IP)

The TCP/IP model is also referred to as the Internet Protocol suite which mainly includes TCP, IP and UDP (User Datagram Protocol, to be discussed shortly). In comparison to the OSI model, the TCP/IP model combines multiple layers into one layer

Layers:

- Application
  - HTTP, SMTP, FTP, DNS
- Transport
  - TCP, UDP
- Internet
  - IP, ICMP, IGMP, ARP, RARP
- Link
  - Ethernet, PPP, Frame Relay, ATM
- Physical
  - Ethernet, Wi-Fi, Bluetooth, DSL, ISDN

## Communication  Protocols

- A protocol is a set of rules that governs the communication between two or more devices

### Network Layer Protocols

- Internet Protocol (IP)
  - IP is responsible for routing data packets from source IP addresses to destination IP addresses
  - IPv4 and IPv6
  - Each packet contains IP Header and Payload
    - ip header contains source and destination IP addresses + other metadata
    - payload contains the actual data - ip datagram
- Internet Control Message Protocol (ICMP)
  - used for network diagnostics and error reporting
  - ICMP messages are encapsulated within IP packets

### Transmission Control Protocol

- TCP is a connection-oriented protocol that provides reliable data delivery
- capability to retransmit data in case of packet loss
- three-way handshake
  - SYN, SYN-ACK, ACK

### User Datagram Protocol

- less reliable but faster data delivery
- no three-way handshake
- no retransmission of lost packets
- used for real-time applications like VoIP, video streaming, and online gaming where speed is more important than reliability

### Hypertext Transfer Protocol

- HTTP is a protocol used for transmitting hypertext documents over the internet
- HTTP/1.1 and HTTP/2
- HTTP/1.1 is a text-based protocol that uses TCP as the transport layer
- HTTP/2 - optimized for performance and speed
  - multiplexing, header compression, and server push
- HTTP/3 is based on the QUIC protocol and uses UDP instead of TCP
- methods: GET, POST, PUT, DELETE, PATCH, OPTIONS, HEAD
- status codes: 1xx, 2xx, 3xx, 4xx, 5xx
  - 1xx: Informational
  - 2xx: Success
  - 3xx: Redirection
  - 4xx: Client Error
  - 5xx: Server Error

###  Simple Mail Transfer Protocol

- SMTP is a protocol used for sending and receiving email
- SMTP uses TCP port 25
- SMTP commands: HELO, MAIL FROM, RCPT TO, DATA, QUIT

### Extensible Messaging and Presence Protocol

- XMPP is a protocol used for real-time communication
- XMPP uses XML for message exchange
- XMPP is used in instant messaging, voice over IP, and social networking applications
- XMPP uses TCP port 5222  for plain text and 5223 for encrypted communication
- XMPP is decentralized and open-source
- ejabberd, Openfire, and Prosody are popular XMPP servers
- use cases: WhatsApp, Facebook Messenger, Google Talk

### Message Queuing Telemetry Transport

- MQTT is a lightweight messaging protocol used for IoT devices
- based on the publish-subscribe model
- QoS levels:
  - 0: At most once
  - 1: At least once
  - 2: Exactly once

## Communication Types

### Pull Mechanism: HTTP Polling

- client sends a request to the server at regular intervals to check for new data
- HTTP Regular Polling
- HTTP Long Polling

### Push Mechanism: WebSockets

- bi-directional persistent connection between the client and the server

### Push Mechanism: Server Sent Events

- one-way communication from the server to the client
- The SSE is implemented over a long lived HTTP connection to consume any updates or notifications from the server in text format

## Common Communication Protocol Standards

### Remote Procedure Call

- RPC is a protocol used for inter-process communication
- RPC allows a program to execute code on a remote server
- RPC is used in distributed systems, client-server applications, and microservices

### Simple Object Access Protocol

- SOAP is a protocol used for exchanging structured information in web services
- SOAP uses XML for message exchange
- SOAP is based on the request-response model
- SOAP messages are sent over HTTP, SMTP, or TCP
- complex and heavyweight
- being replaced by RESTful APIs

### Representational State Transfer

- REST is an architectural style for designing networked applications
- REST API includes client, server and resources
- REST uses JSON
- RESTful APIs are stateless
- fixed schema

### GraphQL

- allows clients to write a query specific to data retrieved on a single API endpoint
- GraphQL is a query language for APIs
- GraphQL is an alternative to RESTful APIs
- GraphQL is more flexible and efficient than RESTful APIs

### Web Real-Time Communication

- The Web Real-Time Communication (webRTC) offers a mechanism to support audio and video communications in web browsers or mobile applications over the internet by APIs without a requirement to install any specific plugin
- WebRTC is not itself a protocol—it’s a tool working on top of multiple protocols to serve our use-case
-
