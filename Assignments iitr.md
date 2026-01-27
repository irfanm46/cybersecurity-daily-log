## Subjective Question: Network Architecture and Trust-Based Vulnerabilities Scenario

- A company experiences repeated internal network attacks
- Employees report sudden internet slowdowns inside the office
- Users are occasionally redirected to fake login pages
- Network analysis shows abnormal ARP table changes
- Unusual routing behavior is observed
- The attacks are suspected to exploit network trust assumptions rather than malware


## Part 1: Architectural Understanding
How the layered architecture helps security analysis

- The OSI/TCP-IP model divides networking into layers with specific responsibilities
- It helps identify which layer is responsible for a security issue
- It prevents incorrect assumptions such as "no malware means no attack"
- It allows mapping of symptoms to protocol behavior (e.g., ARP issues indicate Layer 2)
- It enables targeted security controls without redesigning the network

Layers most relevant to the reported issue

- The issues mainly occur at Layer 2 and Layer 3

Layer 2 (Data Link Layer)

- Abnormal ARP table changes are observed
- ARP operates at Layer 2
- Ethernet assumes devices on the local network are trustworthy

Layer 2 explains

- Traffic interception
- Local man-in-the-middle attacks
- Internet slowdowns due to traffic passing through an attacker

Layer 3 (Network Layer)

- Unusual routing behavior is detected
- IP routing and packet forwarding occur at Layer 3
- Trust is placed in IP addresses and routing information

Layer 3 explains

- Traffic redirection
- IP spoofing
- Route manipulation or rogue gateways


## Part 2: Trust Assumptions and Vulnerabilities
ARP spoofing and Layer 2 trust assumptions

- ARP maps IP addresses to MAC addresses
- Any device can reply to an ARP request
- ARP replies are trusted without verification
- Attackers can claim to be the gateway or a server
- Victims send traffic to the attacker

Result

- Man-in-the-middle attacks
- Traffic interception without malware

IP spoofing and route manipulation at Layer 3

- Layer 3 assumes IP addresses are genuine
- Routing updates are trusted by default
- Internal networks are assumed to be cooperative

Why this is vulnerable

- IP has no built-in authentication
- Routing protocols prioritize reachability over verification

Result

- Traffic redirection
- Attackers gain control or visibility of network traffic

Impact of these weaknesses

- Man-in-the-middle attacks
- Traffic redirection
- Credential theft using fake login pages

---

## Part 3: Applying Security Reasoning
Control 1: Dynamic ARP Inspection (DAI)

- Layer protected: Layer 2
- Switch verifies ARP messages using trusted information
- Fake ARP replies are blocked
- Prevents ARP spoofing and MITM attacks

Control 2: Network Segmentation and VLANs

- Layer protected: Layer 2 and Layer 3
- Network is divided into smaller segments
- Limits who can see or respond to ARP requests
- Reduces the impact of internal attacks

Control 3: Encrypted and Authenticated Communication (TLS)

- Layer protected: Application Layer
- Encrypts traffic between users and servers
- Prevents attackers from reading or modifying data
- Reduces credential theft and fake login attacks



## Final Summary

- Network attacks exploit trust in Layer 2 and Layer 3 protocols
- These attacks do not require malware
- Security can be improved by adding validation, segmentation, and encryption
- Strong security comes from reducing unnecessary trust in the network
