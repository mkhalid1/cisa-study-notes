<!-- nav:top -->
[Contents](../../README.md#contents) · Previous: [Domain 4: Operations and Business Resilience](operations-and-business-resilience.md) · Next: [How CISA scoring works](../scoring.md)
<!-- /nav:top -->

# Domain 5: Protection of Information Assets

**In one line:** whether the organisation's information is protected by sound frameworks, physical, logical and network controls, encryption, monitoring, and a working incident response.

ISACA weights this domain at **26%**, joint largest with Domain 4, about 39 questions if the split were exact. It is the most technical domain, but the questions still ask you to think as an auditor: which weakness matters most, which evidence shows a control works, which control fits the risk. This guide has 16 practice items because of the domain's weight.

## What it covers

| Part A: Information Asset Security and Control (official topics) | What you need to be able to do |
|---|---|
| Information Asset Security Frameworks, Standards, and Guidelines | Recognise the main frameworks and use them as audit criteria. |
| Physical and Environmental Controls | Assess site, facility and environmental protection. |
| Identity and Access Management | Assess identification, authentication, authorisation and the account lifecycle. |
| Network and End-Point Security | Assess firewalls, segmentation, remote access and device protection. |
| Data Loss Prevention | Assess how sensitive data is kept from leaving. |
| Data Encryption | Understand which encryption protects what. |
| Public Key Infrastructure | Understand certificates, authorities and revocation. |
| Cloud and Virtualized Environments | Assess shared responsibility and virtualisation risks. |
| Mobile, Wireless, and Internet-of-Things Devices | Assess the risks and controls for these devices. |

| Part B: Security Event Management (official topics) | What you need to be able to do |
|---|---|
| Security Awareness Training and Programs | Evaluate training and whether it changes behaviour. |
| Information System Attack Methods and Techniques | Recognise common attacks and their controls. |
| Security Testing Tools and Techniques | Understand scanning, penetration testing and related tools. |
| Security Monitoring Tools and Techniques | Assess SIEM, IDS and log review. |
| Security Incident Response Management | Evaluate incident response plans and their execution. |
| Evidence Collection and Forensics | Understand how evidence is preserved and handled. |

## Key concepts

### Frameworks and standards

| Framework | Use |
|---|---|
| ISO/IEC 27001 | Requirements for an information security management system; certifiable |
| ISO/IEC 27002 | Guidance on security controls |
| NIST Cybersecurity Framework | Outcomes grouped into functions (Govern, Identify, Protect, Detect, Respond, Recover in version 2.0) |
| COBIT | Governance and management of enterprise IT |
| CIS Controls | Prioritised technical safeguards |

Auditors use a framework the organisation has adopted, or a recognised one, as the criteria against which controls are judged.

### Physical and environmental controls

- **Access:** badges, locks, mantraps (two doors so only one person passes at a time, which stops piggybacking and tailgating), guards, visitor logs and escorts, CCTV.
- **Location:** avoid flood plains, ground floors for data centres, obvious signage.
- **Environment:** temperature and humidity monitoring. Low humidity causes static discharge; high humidity causes condensation and corrosion.
- **Power:** UPS for short interruptions and clean power, generators for long outages, surge protection.
- **Fire:** detection (smoke, heat), suppression suited to the area: gas-based clean agents or pre-action and dry-pipe sprinkler systems for equipment rooms, with staff safety and evacuation procedures.

### Identity and access management

- **Identification, authentication, authorisation, accountability.** Each user needs a unique ID so actions can be traced. Shared accounts destroy accountability.
- **Authentication factors:** something you know, have or are. Multi-factor means different types. Phishing-resistant methods such as FIDO2 security keys or passkeys resist credential theft best.
- **Authorisation:** least privilege and need to know, usually through role-based access.
- **Lifecycle:** approved provisioning, changes on role moves (remove old access), prompt deprovisioning for leavers, and periodic access reviews by business owners.
- **Privileged access:** individual admin accounts, vaulted credentials, session logging, just-in-time elevation, and independent review of privileged activity.
- **Single sign-on** reduces password fatigue but makes the one credential more valuable, so protect it with MFA.

### Network and endpoint security

| Control | Purpose |
|---|---|
| Packet-filtering firewall | Allows or blocks by address, port and protocol |
| Stateful firewall | Tracks connections and allows only traffic belonging to permitted sessions |
| Application-level gateway or proxy | Inspects application content |
| Next-generation firewall | Adds application awareness, user identity and threat prevention |
| Screened subnet (DMZ) | A network between external and internal firewalls for public-facing servers |
| Segmentation | Separates networks by sensitivity so a breach in one does not reach all |
| IDS / IPS | Detects, or detects and blocks, malicious traffic |
| VPN | Encrypted tunnel for remote access or site links |
| Network access control | Admits only authorised, healthy devices |
| Endpoint detection and response | Monitors devices for malicious behaviour and supports response |
| Hardening | Remove unneeded services, change defaults, apply baselines |

### Data loss prevention

DLP tools identify sensitive data and watch it at rest (storage scans), in motion (email and web gateways) and in use (endpoints), blocking or alerting on policy breaches. DLP depends on knowing what data is sensitive, so it relies on classification.

### Encryption and PKI

| Need | Method |
|---|---|
| Confidentiality of bulk data | Symmetric encryption such as AES |
| Confidential message to a specific person | Encrypt with the **recipient's public key** (in practice, a symmetric session key encrypted with it) |
| Proof of origin and integrity, nonrepudiation | **Digital signature:** hash the message, sign the hash with the **sender's private key**; anyone verifies with the sender's public key |
| Integrity only | Hashing, such as SHA-256 |
| Secure web sessions | TLS, which uses certificates to authenticate the server and negotiates session keys |

**PKI:** a certificate authority (CA) issues certificates that bind a public key to an identity; a registration authority checks identity first. If a private key is compromised, the certificate is **revoked** and relying parties learn of it through a certificate revocation list (CRL) or the Online Certificate Status Protocol (OCSP). Key management covers generation, storage (often in hardware security modules), rotation, revocation and destruction.

### Cloud and virtualisation

| Model | Provider manages | Customer always manages |
|---|---|---|
| IaaS | Physical hosts, storage, network, hypervisor | Operating systems, applications, data, access |
| PaaS | Also operating systems and runtime | Applications, data, access |
| SaaS | Almost everything, including the application | Data, user access, configuration choices |

The customer always remains accountable for its data and who can access it. Virtualisation risks include hypervisor compromise, VM escape, sprawl of unmanaged VMs and weak separation between tenants.

### Mobile, wireless and IoT

- **Mobile:** mobile device management, encryption, screen locks, remote wipe, app control, separation of work and personal data.
- **Wireless:** WPA3 or WPA2 with enterprise authentication; never WEP or open networks for business data; detect rogue access points.
- **IoT:** change default credentials, patch firmware, segment IoT devices from core networks, monitor them.

### Awareness, attacks and testing

Awareness programmes should be ongoing and role-based, and measured by behaviour (phishing simulation results, incident reports), not attendance.

| Attack | Typical control |
|---|---|
| Phishing and social engineering | Awareness, email filtering, phishing-resistant MFA |
| Malware and ransomware | Endpoint protection, patching, least privilege, offline or immutable backups |
| Denial of service | Capacity, filtering, upstream DDoS protection |
| Injection (SQL and others) | Input validation and parameterised queries |
| Man-in-the-middle | Encryption with certificate validation |
| Password attacks | Strong authentication, lockout or throttling, MFA |
| Privilege escalation | Patching, least privilege, monitoring |

| Test | Answers |
|---|---|
| Vulnerability scan | What known weaknesses exist? |
| Penetration test | Can weaknesses be exploited to reach a goal? |
| Configuration review | Do settings match the baseline? |
| Social engineering test | Will staff give up access or information? |
| War driving | Are there unauthorised or weak wireless networks? |

Any active test needs written authorisation and agreed scope.

### Monitoring and incident response

SIEM systems collect and correlate logs and raise alerts; IDS and IPS watch traffic; UEBA flags unusual user behaviour. Monitoring only works if alerts are reviewed and acted on.

Incident response phases, in a common form: **preparation, identification, containment, eradication, recovery, lessons learned.** The plan should define roles, escalation, communication (including legal and regulatory notification), and be tested.

### Evidence and forensics

Preserve evidence before analysing it. Capture volatile data such as memory first, image disks bit for bit using a **write blocker**, hash originals and copies to prove they match, and work only on copies. Keep a **chain of custody** that records every person who handled the evidence, when and why. Involve legal counsel and, where needed, law enforcement.

## How the questions look

Expect audit findings and scenarios about access, networks, encryption, cloud and incidents. Questions ask what is the GREATEST concern, which control BEST addresses a risk, what evidence shows a control works, or what the auditor or response team should do FIRST. Technical depth is modest; judgement about risk is what is tested.

## A method that works

1. **Name the asset and the threat.** What could go wrong, to what data?
2. **Match the control to the risk.** Confidentiality, integrity, availability, accountability?
3. **For access, follow the lifecycle.** Joiner, mover, leaver, review, privileged use.
4. **For crypto, write who holds which key.** Recipient's public key for secrecy; sender's private key for signatures.
5. **For cloud, check the service model** before deciding who is responsible.
6. **For incidents and evidence, preserve and contain first.**
7. **As the auditor, report.** Assess, evidence and recommend.

## Traps that cost points

- **Treating shared admin accounts as a minor issue.** They destroy accountability.
- **Encrypting with the wrong key.** Secrecy uses the recipient's public key; signatures use the sender's private key.
- **Thinking hashing gives confidentiality.** It gives integrity.
- **Thinking a SaaS provider is responsible for your users' access.** Access and data stay with the customer.
- **Placing public servers on the internal network.** They belong in a screened subnet.
- **Choosing a scan when the question asks whether a weakness can be exploited.** That is a penetration test.
- **Skipping containment in an incident.** Contain before eradicating or recovering.
- **Imaging a drive without a write blocker.** The original can be altered, damaging admissibility.
- **Measuring awareness by attendance.** Measure behaviour.
- **Leaving IoT defaults unchanged.** Default credentials are among the first things attackers try.

## Timing

As guidance, 60 to 80 seconds per item. Technical recall items are quick; findings that ask for the GREATEST concern take longer because several options are weaknesses. Rank them by likelihood and impact on sensitive data.

## Practice items

These 4 items are original, written for these notes. They are not taken from ISACA or any prep provider.

### Set 1

**Item 1.** An IS auditor reviews access to the production customer database. Which finding is the GREATEST concern?

- A. Application developers have permanent, unmonitored write access to the production data
- B. Passwords expire every 90 days
- C. Users must contact the help desk to unlock their accounts after five failed login attempts in a row
- D. Access reviews are performed every six months

**Item 2.** Tom wants to send Priya a file that only Priya can read. With which key should the file, or the session key protecting it, be encrypted?

- A. Tom's private key
- B. Tom's public key
- C. Priya's public key
- D. Priya's private key

**Item 3.** A company uses a SaaS application for HR. Which responsibility remains with the company?

- A. Patching the application code
- B. Securing the provider's hypervisors
- C. Managing which users have access and what data is stored
- D. Physical security of the provider's data centres

**Item 4.** The audit committee wants to know whether an attacker could use the weaknesses in a recent scan report to reach payroll data. What should the IS auditor recommend?

- A. A penetration test targeting payroll data, under written authorisation
- B. A repeat of the vulnerability scan with more plug-ins enabled and credentialed access to every server
- C. A review of the firewall rule base only
- D. A staff survey on security awareness

<details>
<summary>Answers and explanations, items 1 to 4</summary>

**Item 1: A.** Developers with standing, unmonitored write access to production data can change customer records without approval or trace, which breaks segregation of duties and integrity. *Why not D:* six-monthly reviews may be enough depending on risk; the developer access is a direct weakness. *Why not B:* a 90-day expiry is a normal setting.

**Item 2: C.** Encrypting with Priya's public key means only her private key can decrypt it. *Why not A:* anything encrypted with Tom's private key can be decrypted by anyone with his public key, which gives no secrecy. *Why not D:* Tom does not have Priya's private key and should never have it.

**Item 3: C.** In SaaS the provider runs the application and infrastructure, but the customer still controls its users' access and its data. *Why not A:* the provider patches its own application. *Why not B:* hypervisors are part of the provider's infrastructure.

**Item 4: A.** A penetration test shows whether weaknesses can actually be exploited to reach a target, which is what the committee asked. *Why not B:* a deeper scan still only lists weaknesses. *Why not C:* a firewall review covers one control, not whether the weaknesses can be chained together.

</details>

Want more? The [free timed CISA practice test on PrepClubs](https://prepclubs.com/free-practice-tests/cisa?utm_source=github&utm_medium=referral&utm_campaign=6n8cun&utm_content=cisa) has 25 questions across all five domains, with your score broken down by domain.

## Score yourself

| Item | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Answer | A | C | C | A |

- **4:** strong. Keep the encryption and cloud rules fresh.
- **3:** sort misses into technical controls and judgement, and drill the tables for the weaker side.
- **2 or fewer:** rebuild the encryption, cloud and attack tables from memory, then redo the items.

## Next step

Domain 5 rewards fast recall plus calm judgement. Try both in the [free CISA practice test on PrepClubs](https://prepclubs.com/free-practice-tests/cisa?utm_source=github&utm_medium=referral&utm_campaign=6n8cun&utm_content=cisa), then return to the traps list.

## Sources for this page

- [ISACA CISA exam content outline](https://www.isaca.org/credentialing/cisa/cisa-exam-content-outline), for the topics and weight

---

<!-- nav:bottom -->
← Previous: [Domain 4: Operations and Business Resilience](operations-and-business-resilience.md) | Next: [How CISA scoring works](../scoring.md) → | [Back to contents](../../README.md#contents)
<!-- /nav:bottom -->
