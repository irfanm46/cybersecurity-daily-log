# cybersecurity-daily-log
Daily cybersecurity learning notes

## Day 1 – SOC Basics

- Learned what a SOC Analyst does daily
- Understood alert vs incident difference
- Explored common log sources
- Studied basic incident response flow
- Focused on importance of documentation
- 
PART 1 — WHAT CYBERSECURITY ACTUALLY IS (NO BUZZWORDS)

Most beginners think cybersecurity is about:
Hackers
Tools
Attacks
That’s wrong.

🔑 Cybersecurity is about protecting trust
Trust that:
Money is correct
Data is private
Systems work when needed
If trust breaks → real-world damage happens.
Everything you studied fits into this single sentence:
Cybersecurity ensures the right data, is accessed by the right people, at the right time, in the right way.
Now let’s break the system.

PART 2 — THE CIA TRIAD (THE FOUNDATION OF EVERYTHING)

Think of the CIA Triad as the laws of physics for security.
Every control, tool, framework exists to protect one or more of these.

1️⃣ Confidentiality — “Who is allowed to see this?”
This is access control.
Mental model
If data is seen by someone who shouldn’t → confidentiality failed.
Not stolen. Just seen. That’s enough.
Real examples
Someone reads your email
Employee accesses salary records
Cloud storage exposed publicly
How professionals enforce it
Authentication (prove identity)
Authorization (what you’re allowed to do)
Encryption (even if stolen, unreadable)

🔴 Common beginner mistake
Thinking confidentiality = passwords only
→ In reality, misconfigurations cause more leaks than hacking

2️⃣ Integrity — “Can I trust this data?”

Integrity is about unchanged truth.

Mental model
If data is modified silently → integrity failed.
This is subtle but deadly
Bank balance altered
Logs edited
Software modified
Even 1-bit change = integrity failure.
How professionals protect integrity
Hashing (detects changes)
Digital signatures (prove origin + integrity)
Logs (who changed what and when)

🔴 Important insight
Attackers love integrity attacks because:
Systems still “work”
Damage is silent
Trust erodes slowly

3️⃣ Availability — “Does it work when needed?”

Availability is business survival.
Mental model
Secure but unusable = still a failure.
Examples:
Exam portal down
Hospital system offline
Ransomware locks files
How availability is protected
Backups
Redundancy
Monitoring
DDoS protection

🔴 Reality check
Most companies feel availability pain first, not data theft.

🔥 CIA TRIAD INSIGHT (THIS IS INTERVIEW GOLD)
Security is not about maximizing one pillar — it’s about balancing all three.
Maximum confidentiality can kill availability
Maximum availability can weaken confidentiality
Security is trade-offs, not perfection.
PART 3 — WHO ATTACKS SYSTEMS (THREAT ACTORS)
Attacks are not random.
They are motivated, predictable, and patterned.
Why categorization matters
Because defenses depend on the attacker, not just the attack.
🧑‍💻 Script Kiddies
Low skill
High noise
Use public tools
Defense: Basic hygiene stops them

💰 Cybercriminals
Money-driven
Organized
Scalable attacks
Defense: Monitoring + response speed

🏢 Insiders (MOST DANGEROUS)
Already trusted
Already inside
May be careless or malicious
Defense: Least privilege + logging

📢 Hacktivists
Ideology-driven
Want visibility
Target reputation
Defense: Web security + monitoring

🏛️ Nation-State
Stealthy
Long-term
Strategic goals
Defense: Architecture + layered security

🔑 Pro insight
Security is not about stopping all attackers.
It’s about limiting impact based on attacker type.

PART 4 — ATTACK VECTORS (HOW THEY GET IN)
Attack vectors are paths, not magic.
Most attacks succeed because:
Humans trust too much
Permissions are excessive
Systems are unpatched
Common vectors
Phishing
Weak passwords
Misconfigurations
Excess access
Unpatched software

🔴 Important truth

Complexity doesn’t cause breaches.
Neglect does.

PART 5 — DEFENSE-IN-DEPTH (THE CORE STRATEGY)

This is how professionals think.

Mental model

Assume failure. Plan containment.

Not:

“This control will never fail”

But:

“When this fails, what stops total damage?”

Layers typically include

Network controls

Identity controls

Application controls

Monitoring

Backups

🔑 Key idea

Attackers must pass multiple gates, not one door.

PART 6 — LEAST PRIVILEGE (DAMAGE CONTROL)

Least Privilege is blast-radius reduction.

Mental model

Assume compromise. Minimize damage.

Examples:

Intern ≠ admin

Service ≠ full database access

Temporary access ≠ permanent

🔴 This principle protects

Confidentiality

Integrity

Availability

One concept → protects all three.

PART 7 — ZERO TRUST (MODERN REALITY)

Zero Trust is not a tool.
It’s a mindset.

Old model

Inside network = trusted

New reality

Cloud

Remote work

Personal devices

Zero Trust rule

Never trust by default. Always verify.

This means:

Identity matters more than location

Every request is checked

Breaches are assumed

🔑 Pro insight

Zero Trust enforces Defense-in-Depth and Least Privilege continuously.

PART 8 — CYBERSECURITY FRAMEWORKS (HOW ADULTS DO SECURITY)

Frameworks exist because:

Tools without structure fail

People panic without plans

What frameworks really do

They organize thinking, not tools.

The Universal Lifecycle (MEMORIZE THIS FLOW)

1️⃣ Identify – What matters
2️⃣ Protect – Reduce risk
3️⃣ Detect – Notice issues
4️⃣ Respond – Control damage
5️⃣ Recover – Restore + improve

This cycle never ends.

NIST vs ISO vs CIS (CLEAR DIFFERENCE)

NIST → Risk & lifecycle thinking

ISO 27001 → Governance & proof

CIS → Practical technical actions

They complement, not compete.

PART 9 — NETWORKING (WHY SECURITY STARTS HERE)

If you don’t understand:

How data moves

How addresses work

How protocols behave

You cannot defend networks.

=Core insight

=Attacks exploit protocol behavior, not just bugs.

TCP, UDP, DNS, ICMP exist for functionality, not security.
Security is layered on top.

That’s why:

Encryption matters

Monitoring matters

Architecture matters

FINAL MENTAL MODEL (THIS TIES EVERYTHING)

Think like this:

CIA Triad = What to protect

Threat actors = Who attacks

Attack vectors = How they enter

Defense-in-depth = How we survive failure

Least privilege = How we limit damage

Zero Trust = How we remove assumptions

Frameworks = How we stay sane

Networking = Where attacks actually happen

🎓 FINAL TAKEAWAY (READ THIS TWICE)

Cybersecurity is not about hacking systems.
It is about designing systems that fail safely.

This mindset is what:

SOC teams use

Architects use

                                                                                                                    23-01-26
                                                                                                                    
Learnt about SOC - Security Operations Center (ANALYST)                                                                                                                   
did some LABS in tryhackme.com


Room: SOC Fundamentals

What was the alert?
- Example: Suspicious login / malware / phishing

What data did I check?
- Logs, timestamps, source IP, user context

What decision did I make?
- True positive / False positive / Needs escalation

Why?
- Explain in 3–4 lines

What would I do next in a real SOC?
- Containment / Monitoring / Escalation


## Pre-Read: Network Traffic Forensics Concepts (Becoming a Network Detective)
🌟 Why This Session Matters
When a cyber attack happens, one question always comes first:

What actually happened on the network?

Files can be deleted. Logs can be altered. But network traffic leaves traces.

Network forensics is the art of reading those traces.

This session teaches you how security professionals reconstruct digital events by studying network traffic.

📦 Packets Are Digital Evidence
Every message sent across a network becomes a packet.

Packets carry:

Sender and receiver information
Timing details
Protocol details
Instructions on how data should be handled
To a normal user, packets are invisible.

To a security analyst, packets are evidence.

By examining packet details, analysts can answer:

Who talked to whom
What kind of data was exchanged
Whether communication was normal or suspicious
🧭 Following the Flow
Looking at one packet is useful. But looking at many packets together tells the full story.

This is called flow analysis.

A flow shows:

How long communication lasted
How much data moved
Which direction data traveled
Whether the pattern looks normal
For example:

A short burst of data may be normal browsing. A long silent connection sending data outward may indicate data theft.

Recognizing these patterns is key to network forensics.

🚨 Detecting Known Threat Signatures
Some attacks follow known patterns.

Certain scans. Certain malware communications. Certain suspicious behaviors.

Security tools look for these known fingerprints, often called signatures.

When traffic matches a known signature, alarms are triggered.

This session helps you understand the logic behind signature detection, not just how tools do it.

🧠 The Hidden Clues Inside Packet Headers
A packet is like a postal envelope.

The envelope carries:

Sender address
Receiver address
Type of delivery
Sequence numbers
Control flags
Inside these header details lie clues.

=Was the sender pretending to be someone else
=Was the connection completed correctly
==Was the message fragmented strangely
=Learning to read headers teaches you to spot inconsistencies that signal attacks.

🧪 What You Will Learn in This Session
You will understand:

=How traffic flows reveal behavior
=How signature detection concepts work
=What metadata exists in network communications
=How to interpret packet headers for security diagnosis
=By the end, you will be able to explain why a piece of traffic looks normal or suspicious.

This is a critical skill for security operations and incident response teams.

💭 Before the Session
Think about this:

If someone secretly copied files from a company, what network traces might appear
How could you tell normal web browsing from data exfiltration
Why might attackers try to hide inside normal looking traffic
Bring these thoughts to class. They will sharpen your investigative mindset.

✨ Closing Thought
Hackers write malicious code. Defenders read malicious traffic.

This session is your step into the mindset of a cybersecurity investigator.


##DEEP PATTERN ANALYSIS

##Wireshark can capture the pockets of the target system by getting tcp,dcp,http and some packets 

##cyberchef is the tool used for decoding the mails


Wireshark????
its a tool.to capture pockets and pockets of infos
##Need to re-watch IM Session 6 - Workshop: Applied Network Security Analysis (30-01-26)