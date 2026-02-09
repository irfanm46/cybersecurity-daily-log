# Cybersecurity Daily Log & SOC Foundations:

This repository documents my hands-on learning and conceptual understanding of cybersecurity, with a strong focus on **Security Operations Center (SOC)** practices, incident analysis, and defensive security thinking.

The content is structured to reflect how SOC analysts reason about security problems in real-world environments.

---

## SOC Foundations – Day 1:

### Key Learnings
- Understood the daily responsibilities of a SOC Analyst (L1)
- Differentiated between **alerts** and **incidents**
- Explored common log sources used in SOC environments
- Studied the basic incident response lifecycle
- Learned the importance of clear documentation in security operations.

---

## What Cybersecurity Actually Is:

Cybersecurity is not about tools, exploits, or attackers.

**Cybersecurity is about protecting trust.**

Trust that:
- Financial data is correct  
- Sensitive data is private  
- Systems function when needed  

When trust breaks, real-world damage occurs.

**Core principle:**  
Cybersecurity ensures the right data is accessed by the right people, at the right time, in the right way.

---

## The CIA Triad – Security Fundamentals

The CIA Triad forms the foundation of all security controls and frameworks.

### Confidentiality
- Ensures data is only accessible to authorized entities
- Enforced through authentication, authorization, and encryption
- Common failures result from misconfigurations, not hacking

### Integrity
- Ensures data remains accurate and unaltered
- Protected through hashing, digital signatures, and logging
- Integrity attacks are dangerous because damage can remain unnoticed

### Availability
- Ensures systems are operational when required
- Protected through backups, redundancy, monitoring, and DDoS mitigation
- Availability failures are often felt before data breaches

**Key Insight:**  
Security is about balance. Over-prioritizing one pillar can weaken the others.

---

## Threat Actors – Who Attacks Systems

Security defenses depend on **who the attacker is**, not just the technique.

### Common Threat Actors
- **Script Kiddies** – Low skill, high noise
- **Cybercriminals** – Financially motivated, organized
- **Insiders** – Trusted users with access (highest risk)
- **Hacktivists** – Ideology-driven, reputation focused
- **Nation-State Actors** – Long-term, stealthy, strategic

**Key Insight:**  
Security is not about stopping every attacker, but limiting impact based on attacker type.

---

## Attack Vectors – How Attacks Begin

Attack vectors are not complex magic; they are paths created by neglect.

### Common Vectors
- Phishing
- Weak passwords
- Excessive permissions
- Misconfigurations
- Unpatched systems
- Restarting

**Important Truth:**  
Complexity doesn’t cause breaches — neglect does.

---

## Defense in Depth – Core Security Strategy

Security controls are designed with failure in mind.

**Mindset:**  
Assume breach. Plan containment.

### Common Layers:
- Network controls
- Identity and access controls
- Application security
- Monitoring and logging
- Backups and recovery

Attackers must bypass multiple layers, not a single control.

---

## Least Privilege – Damage Control

Least privilege minimizes the blast radius of compromise.

### Examples
- Intern ≠ administrator
- Services ≠ full database access
- Temporary access ≠ permanent access

This single principle protects:
- Confidentiality
- Integrity
- Availability

---

## Zero Trust – Modern Security Model

Zero Trust is a mindset, not a tool.

### Core Rules
- Never trust by default
- Always verify
- Assume breach

Identity matters more than network location, especially in cloud and remote environments.

---

## Cybersecurity Frameworks – Structured Security

Frameworks exist to prevent chaos during incidents.

### Universal Security Lifecycle
1. Identify
2. Protect
3. Detect
4. Respond
5. Recover

### Framework Comparison
- **NIST** – Risk and lifecycle focused
- **ISO 27001** – Governance and compliance
- **CIS Controls** – Practical technical guidance
gets hands on practice. 
Frameworks complement each other rather than compete.

---

## Networking – Where Security Actually Happens

Understanding networking is essential for security analysis.

Attackers exploit protocol behavior, not just vulnerabilities.

Protocols such as TCP, UDP, DNS, and ICMP are designed for functionality, not security.  
Security is layered on top through encryption, monitoring, and architecture.

---

## SOC Investigation Workflow (Practiced)

Room: **SOC Fundamentals – TryHackMe**

### Investigation Questions
- What triggered the alert?
- What data was analyzed (logs, IPs, timestamps, user context)?
- What decision was made?
  - True Positive
  - False Positive
  - Needs Escalation
- Why was that decision made?
- What would be the next action in a real SOC?
  - Containment
  - Monitoring
  - Escalation

---

## Network Traffic Forensics – Pre-Read Summary

Network traffic provides durable evidence even when files or logs are altered.

### Key Concepts
- Packets carry metadata, timing, and protocol information
- Flow analysis reveals behavior patterns over time
- Signature detection identifies known malicious patterns
- Packet headers expose inconsistencies and anomalies

**Analyst Mindset:**  
Hackers write malicious code. Defenders read malicious traffic.

---

## Tools & Concepts Encountered
- Wireshark – Network packet analysis
- CyberChef – Decoding and data transformation
- Indicators of Compromise (IOC)
- TTPs – Tactics, Techniques, and Procedures
- SIEM, EDR, and Firewall integration (lab exposure)

---

## Final Takeaway:

Cybersecurity is not about hacking systems.

It is about **designing systems that fail safely**.

This mindset is used by:
- SOC teams
- Incident responders
- Security architects


Cyber Threat Landscape – Summary Notes
Role of Threat Intelligence
• Moves beyond generic alerts to provide actionable, contextual insights
• Enables proactive defense and informed decision-making
• Helps organizations focus on threats that are relevant to their environment
Key Questions Addressed by Threat Intelligence
• Who is targeting whom?
– Identifies threat actors based on capability, motivation, geography, and industry focus
• Why are they targeting?
– Understands adversary objectives such as financial gain, espionage, disruption, or strategic advantage
• What capabilities do they use?
– Maps adversary tools, techniques, and procedures (TTPs) to strengthen detection and defenses
Benefits
• Enables proactive defense by anticipating attacker behavior
• Supports prioritization of security investments based on real-world threats
Expansion of the Attack Surface
• Digital transformation increases the number of exploitable entry points
• Every new technology adoption introduces potential vulnerabilities
Key Attack Surface Drivers
• Cloud Adoption
– New security boundaries and shared responsibility challenges
• Remote Work
– Distributed workforce operating outside traditional network perimeters
• IoT & OT Systems
– Internet-connected devices with limited built-in security controls
• Third-Party Dependencies
– Reliance on external vendors and integration partners
• Supply Chains
– Complex ecosystems with inconsistent security postures
Advanced Persistent Threats (APTs)
• Represent the most sophisticated category of cyber threats
• Focus on long-term strategic objectives rather than immediate financial gain
• Operations often persist undetected for months or years
Defining Characteristics of APTs
• Highly Skilled Operators
– Deep technical expertise, often state-sponsored or well-funded
• Custom Tooling
– Bespoke malware and exploits designed to evade detection
• Patience and Persistence
– Slow, methodical operations to maintain long-term access
Strategic Value Focus
• Targets include intellectual property, classified data, strategic communications, and critical infrastructure
• Primary goal is long-term political, military, or economic advantage
• Key distinction: APTs accept higher cost and longer timelines for strategic impact
Learning Outcomes
• Understand the evolution of modern cyber threats
• Differentiate between cybercriminals and nation-state threat actors
• Identify defining traits of Advanced Persistent Threats
• Apply strategic context to assess business risk and support executive decision-making