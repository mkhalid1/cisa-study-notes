<!-- nav:top -->[Contents](../../README.md#contents) · Previous: [Domain 4: Operations and Business Resilience](operations-and-business-resilience.md) · Next: [How CISA scoring works](../scoring.md)<!-- /nav:top -->

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

These 16 items are original, written for these notes. They are not taken from ISACA or any prep provider.

### Set 1

**Item 1.** An IS auditor reviews access to the production customer database. Which finding is the GREATEST concern?

- A. Application developers have permanent, unmonitored write access to the production data
- B. Passwords expire every 90 days
- C. Users must contact the help desk to unlock their accounts after five failed login attempts in a row
- D. Access reviews are performed every six months

**Item 2.** Priya receives a digitally signed contract from Tom. Which key does Priya use to verify Tom's signature?

- A. Priya's private key
- B. Tom's public key
- C. Tom's private key
- D. Priya's public key

**Item 3.** Tom wants to send Priya a file that only Priya can read. With which key should the file, or the session key protecting it, be encrypted?

- A. Tom's private key
- B. Tom's public key
- C. Priya's public key
- D. Priya's private key

**Item 4.** The private key behind a company's web server certificate has been stolen. What MOST directly stops browsers and partners from continuing to trust that certificate?

- A. Changing the web server's administrator password
- B. Moving the web server to a new IP address
- C. Issuing a new certificate for the server and leaving the old one valid until its expiry date
- D. Revoking the certificate so that its status is published through a CRL or OCSP

<details>
<summary>Answers and explanations, items 1 to 4</summary>

**Item 1: A.** Developers with standing, unmonitored write access to production data can change customer records without approval or trace, which breaks segregation of duties and integrity. *Why not D:* six-monthly reviews may be enough depending on risk; the developer access is a direct weakness. *Why not B:* a 90-day expiry is a normal setting.

**Item 2: B.** A signature made with Tom's private key is verified with Tom's public key. *Why not C:* only Tom has his private key. *Why not A:* Priya's private key decrypts messages sent to her, not signatures from others.

**Item 3: C.** Encrypting with Priya's public key means only her private key can decrypt it. *Why not A:* anything encrypted with Tom's private key can be decrypted by anyone with his public key, which gives no secrecy. *Why not D:* Tom does not have Priya's private key and should never have it.

**Item 4: D.** Revocation, published through a CRL or OCSP, tells relying parties not to trust the certificate. *Why not C:* leaving the old certificate valid lets the thief impersonate the server until it expires. *Why not A:* the stolen key works regardless of the admin password.

</details>

### Set 2

**Item 5.** Staff often hold the data centre door open for colleagues behind them. Which control BEST prevents this piggybacking?

- A. A mantrap that lets only one person through at a time
- B. A sign reminding staff not to hold the door
- C. A CCTV camera recording the door, with footage reviewed by security each week
- D. A visitor log at reception

**Item 6.** Monitoring shows unusually low humidity in the server room. What is the MAIN risk?

- A. Condensation forming on equipment
- B. Static electricity damaging components
- C. Faster wear of fire suppression systems
- D. Corrosion of circuit boards

**Item 7.** Where should a company's public-facing web servers be placed?

- A. On the internal network with the file servers, protected by the same perimeter firewall
- B. In a screened subnet (DMZ) between the external and internal firewalls
- C. Directly on the internet with no firewall in front
- D. On the same network segment as the database servers

**Item 8.** An IS auditor wants to confirm that controls stop employees emailing customer card numbers outside the company. Which control should the auditor expect to test?

- A. Full-disk encryption on laptops
- B. A web application firewall
- C. Data loss prevention at the email gateway
- D. A network access control system

<details>
<summary>Answers and explanations, items 5 to 8</summary>

**Item 5: A.** A mantrap physically lets only one person through at a time, which prevents piggybacking. *Why not C:* CCTV records the event but does not stop it. *Why not B:* a sign depends on behaviour, which is what is failing.

**Item 6: B.** Low humidity allows static to build up, which can damage electronics. *Why not A:* condensation is a risk of high humidity. *Why not D:* corrosion also comes from high humidity.

**Item 7: B.** A screened subnet exposes public servers to the internet under firewall control while keeping them separate from internal systems. *Why not A:* a compromised web server on the internal network would give direct access to internal systems. *Why not C:* no firewall leaves the servers fully exposed.

**Item 8: C.** DLP at the email gateway inspects outgoing messages for sensitive data such as card numbers and blocks or alerts. *Why not A:* disk encryption protects data at rest if a laptop is lost, not data being emailed. *Why not B:* a WAF protects web applications from incoming attacks.

</details>

### Set 3

**Item 9.** A company uses a SaaS application for HR. Which responsibility remains with the company?

- A. Patching the application code
- B. Securing the provider's hypervisors
- C. Managing which users have access and what data is stored
- D. Physical security of the provider's data centres

**Item 10.** Which single control BEST reduces the impact of staff entering their passwords into phishing sites?

- A. Requiring longer passwords
- B. Changing passwords every 30 days
- C. Annual security awareness training with a short quiz at the end
- D. Phishing-resistant multi-factor authentication such as security keys

**Item 11.** The audit committee wants to know whether an attacker could use the weaknesses in a recent scan report to reach payroll data. What should the IS auditor recommend?

- A. A penetration test targeting payroll data, under written authorisation
- B. A repeat of the vulnerability scan with more plug-ins enabled and credentialed access to every server
- C. A review of the firewall rule base only
- D. A staff survey on security awareness

**Item 12.** An incident response plan lists identification as the first step after preparation. Which step should come next?

- A. Eradication
- B. Recovery
- C. Containment
- D. Lessons learned

<details>
<summary>Answers and explanations, items 9 to 12</summary>

**Item 9: C.** In SaaS the provider runs the application and infrastructure, but the customer still controls its users' access and its data. *Why not A:* the provider patches its own application. *Why not B:* hypervisors are part of the provider's infrastructure.

**Item 10: D.** Phishing-resistant MFA, tied to the real site, means a stolen password alone is useless and the key will not work on a fake site. *Why not C:* training lowers how often people fall for phishing but cannot stop every case. *Why not A:* a longer password is just as easy to type into a fake page.

**Item 11: A.** A penetration test shows whether weaknesses can actually be exploited to reach a target, which is what the committee asked. *Why not B:* a deeper scan still only lists weaknesses. *Why not C:* a firewall review covers one control, not whether the weaknesses can be chained together.

**Item 12: C.** Once an incident is identified, containment stops it spreading. Eradication and recovery follow. *Why not A:* eradicating before containing lets the attack continue elsewhere. *Why not D:* lessons learned come last.

</details>

### Set 4

**Item 13.** A forensic examiner copied a suspect's hard drive by connecting it directly to a workstation without any protection against writes. What is the GREATEST concern?

- A. The copy may take much longer than it would with specialised forensic imaging hardware
- B. The original drive may have been altered, weakening the evidence
- C. The workstation may run out of storage
- D. The examiner may need to repeat the copy later

**Item 14.** An IS auditor finds wireless access points in a branch office still using WEP. Why is this the GREATEST concern among wireless settings?

- A. WEP access points usually need more frequent firmware updates than newer models do
- B. WEP reduces the range of the wireless network
- C. WEP does not support guest networks
- D. WEP's encryption can be broken quickly, exposing traffic and network access

**Item 15.** Database administrators all log in with one shared administrator account. What is the GREATEST concern?

- A. Actions cannot be traced to an individual, so accountability is lost
- B. The account password may be hard to remember
- C. The administrators may need to log in and out more often during the working day
- D. The shared account uses more licences

**Item 16.** Smart cameras and sensors in a factory still use their default usernames and passwords. What should the IS auditor recommend FIRST?

- A. Replace every device with a newer model
- B. Turn off all of the devices until a new, separate factory network has been designed and built
- C. Ask the device vendor to monitor the devices
- D. Change the default credentials and move the devices onto a separate network segment

<details>
<summary>Answers and explanations, items 13 to 16</summary>

**Item 13: B.** Without a write blocker, the operating system may write to the original drive, so the evidence's integrity can be challenged. *Why not A:* speed is a convenience, not an evidential issue. *Why not D:* repeating the copy does not fix any change already made to the original.

**Item 14: D.** WEP's weaknesses let attackers recover keys quickly and read traffic or join the network. *Why not B:* range is not the issue. *Why not A:* firmware frequency is minor compared with broken encryption.

**Item 15: A.** With a shared account, no action can be tied to one person, which undermines accountability, investigations and segregation of duties. *Why not B:* memorability is minor. *Why not D:* licensing is a cost issue, not a control issue.

**Item 16: D.** Changing defaults removes the easiest attack, and segmentation limits damage if a device is compromised. Both are quick and proportionate. *Why not A:* replacement may not be needed and takes time. *Why not B:* shutting down production equipment is disproportionate when simpler fixes exist.

</details>

## Score yourself

| Item | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 | 13 | 14 | 15 | 16 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| Answer | A | B | C | D | A | B | B | C | C | D | A | C | B | D | A | D |

- **15 to 16:** strong. Keep the encryption and cloud rules fresh.
- **11 to 14:** sort misses into technical controls and judgement, and drill the tables for the weaker side.
- **10 or fewer:** rebuild the encryption, cloud and attack tables from memory, then redo the items.

## Next step

Domain 5 rewards fast recall plus calm judgement. Try both in the [free CISA practice test on PrepClubs](https://prepclubs.com/free-practice-tests/cisa?utm_source=github&utm_medium=referral&utm_campaign=study-notes&utm_content=cisa), then return to the traps list.

## Sources for this page

- [ISACA CISA exam content outline](https://www.isaca.org/credentialing/cisa/cisa-exam-content-outline), for the topics and weight

---

<!-- nav:bottom -->← Previous: [Domain 4: Operations and Business Resilience](operations-and-business-resilience.md) | Next: [How CISA scoring works](../scoring.md) → | [Back to contents](../../README.md#contents)<!-- /nav:bottom -->
