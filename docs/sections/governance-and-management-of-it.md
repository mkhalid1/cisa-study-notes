<!-- nav:top -->[Contents](../../README.md#contents) · Previous: [Domain 1: Information Systems Auditing Process](information-systems-auditing-process.md) · Next: [Domain 3: Acquisition, Development and Implementation](acquisition-development-and-implementation.md)<!-- /nav:top -->

# Domain 2: Governance and Management of IT

**In one line:** whether IT is directed by the business, organised sensibly, run within its risk appetite, and measured against what it promised to deliver.

ISACA weights this domain at **18%**, about 27 questions if the split were exact. It is where the CISA tests whether you can see the organisation from the board's side: strategy, structure, policy, risk, vendors and performance. Technical knowledge helps little here; understanding who should decide what helps a lot.

## What it covers

| Part A: IT Governance (official topics) | What you need to be able to do |
|---|---|
| Laws, Regulations, and Industry Standards | Judge whether IT complies with obligations that apply to the organisation. |
| Organizational Structure, IT Governance, and IT Strategy | Assess committees, roles, reporting lines and the link between business and IT strategy. |
| IT Policies, Standards, Procedures and Practices | Check the policy hierarchy exists, is approved and is followed. |
| Enterprise Architecture and Considerations | Understand how architecture aligns systems with business needs. |
| Enterprise Risk Management | Assess how IT risk is identified, owned, treated and reported. |
| Privacy Program and Principles | Evaluate how personal data is governed. |
| Data Governance and Classification | Check data has owners, classification and quality controls. |

| Part B: IT Management (official topics) | What you need to be able to do |
|---|---|
| IT Resource Management | People, budgets and assets: hiring, training, segregation, funding. |
| IT Vendor Management | Selection, contracts, monitoring and exit for third parties. |
| IT Performance Monitoring and Reporting | Metrics, scorecards and reporting to management. |
| Quality Assurance and Quality Management of IT | Quality frameworks and continuous improvement. |

## Key concepts

### Governance versus management

| | Governance | Management |
|---|---|---|
| Who | Board and executive leadership | CIO and IT management |
| What | Evaluate options, direct the organisation, monitor performance and risk | Plan, build, run and monitor IT within the direction set |
| Output | Strategy, risk appetite, policy, priorities | Projects, services, operations |

COBIT, ISACA's framework for governance and management of enterprise IT, uses this split. A board that is personally choosing technology products is doing management; a CIO setting the organisation's risk appetite is doing governance. Both are warning signs.

### Committees and roles

| Body | Level | Typical role |
|---|---|---|
| Board of directors | Top | Accountable for governance, including IT |
| Audit committee | Board | Oversees internal and external audit, receives audit reports |
| IT strategy committee | Board | Advises the board on IT strategy and its alignment with the business |
| IT steering committee | Executive | Prioritises and approves IT investments and projects, monitors delivery |
| Change advisory board | Operational | Reviews and approves changes |
| CIO | Executive | Leads IT management |
| CISO | Executive | Leads the security programme |

The IT strategic plan should be derived from the business strategy and approved by the business. An IT plan written in isolation is a governance failure.

### Policies, standards and procedures

Policies are high-level, approved by senior management. Standards set mandatory specifics. Procedures give the steps. Guidelines are optional advice. The auditor checks that each exists, is approved at the right level, is communicated, is reviewed regularly, and is actually followed. An unapproved policy has no authority.

### Enterprise architecture

Enterprise architecture describes how business processes, data, applications and technology fit together, so investments support the strategy. Frameworks such as the Zachman framework and TOGAF give structure. For the auditor, the question is whether architecture decisions are documented and guide projects, or whether systems grow without a plan.

### Enterprise risk management

- **Risk appetite:** the amount and type of risk the organisation is willing to pursue or accept, set by the board.
- **Risk tolerance:** acceptable variation around specific objectives.
- **Risk capacity:** the most risk the organisation could absorb.
- **Inherent risk** exists before controls; **residual risk** remains after them. Residual risk should sit within appetite.
- Each risk needs an **owner** in the business, a response (mitigate, transfer, avoid, accept), and regular reporting, usually through a **risk register**.

### Privacy and data governance

Privacy programmes rest on principles common to most privacy laws: lawful basis and notice, purpose limitation, data minimisation, accuracy, storage limitation, security, individual rights and accountability. Data governance gives every important dataset an **owner** who classifies it and approves access, with stewards maintaining quality. Classification drives handling, retention and protection.

### IT resource management

- **People:** background checks in line with the role, job descriptions, training, and termination procedures that remove access promptly. Mandatory leave and job rotation help detect fraud.
- **Segregation of duties (SoD):** no one person should control a whole sensitive process. Common incompatible pairs: developing and moving code to production; administering security and using the system as an ordinary user; initiating and approving payments; operating systems and changing their programs.
- **Compensating controls** when SoD is not possible, for example in a small team: independent supervisory review of activity logs, exception reports and reconciliations.
- **Financial management:** budgets, chargeback or showback so the business sees IT costs, and investment decisions based on business cases.

### Vendor management

1. **Due diligence** before selection: financial stability, security, capacity, references.
2. **Contract:** scope, service levels, security and privacy requirements, data ownership, breach notification, subcontracting rules, **right to audit** or provision of independent assurance reports, termination and exit, and data return or destruction.
3. **Monitoring:** service level reports, assurance reports such as SOC reports, reviews and issue tracking.
4. **Exit:** transition plans so the organisation is not locked in.

The organisation can outsource the activity but not the accountability. When relying on an assurance report, check that its scope covers the services you use and that its period is current.

### Performance monitoring

The **balanced scorecard** measures IT from four perspectives: financial, customer, internal processes, and learning and growth. **Key performance indicators** measure how well processes perform; **key goal indicators** or outcome measures show whether objectives were achieved. Good metrics are tied to business goals, measurable, and reported to people who can act on them.

### Quality and maturity

Quality management systems such as ISO 9001 define processes and continuous improvement. Maturity or capability models, such as CMMI or COBIT's capability levels, rate how well defined and managed processes are, from ad hoc to optimised. The auditor uses them to judge where a process is and what would improve it.

## How the questions look

Expect governance scenarios: an IT plan, a committee, a policy, an outsourcing contract, a set of metrics. The question asks what concerns the auditor MOST, what is the BEST evidence of good governance, or who should do something. Answers usually favour business ownership, board-level direction, approved and current documents, and measurable oversight.

## A method that works

1. **Ask who should own it.** Board, business owner, IT management, or the auditor? Many items turn on the wrong person making a decision.
2. **Look for the link to business objectives.** Strategies, projects and metrics that are not tied to business goals are the usual GREATEST concern.
3. **Check approval and currency.** Is the document approved at the right level and up to date?
4. **For risk, find the owner and the appetite.** Is residual risk known, owned and within appetite?
5. **For vendors, check the contract and the evidence.** Right to audit, service levels, security terms, and current assurance reports.
6. **For people, look for segregation.** If duties cannot be split, look for compensating controls.

## Traps that cost points

- **Accepting an IT strategy that IT wrote alone.** It must be derived from and approved by the business.
- **Confusing the IT strategy committee and the IT steering committee.** The first advises the board on strategy; the second prioritises projects and investments.
- **Thinking outsourcing transfers accountability.** It does not.
- **Ignoring a missing right-to-audit clause.** Without it, or without assurance reports, you cannot obtain evidence.
- **Choosing a technical fix for a governance problem.** If the policy is not approved, a new tool does not help.
- **Letting IT classify business data.** Data owners classify.
- **Forgetting compensating controls in small teams.** Where SoD is impossible, supervisory review is the expected answer.
- **Treating risk appetite and tolerance as the same.** Appetite is the overall amount the board accepts; tolerance is acceptable variation for specific objectives.

## Timing

As guidance, governance items take 70 to 90 seconds because several options often sound reasonable. Spend the time on reading the stem for who is acting and at what level, then decide.

## Practice items

These 12 items are original, written for these notes. They are not taken from ISACA or any prep provider.

### Set 1

**Item 1.** An IS auditor reviews the IT strategic plan. Which finding is the GREATEST concern?

- A. The plan does not refer to the organisation's business objectives
- B. The plan uses a lot of technical language that the board may find hard to read
- C. The plan covers a three-year period and is refreshed every year
- D. The plan was drafted by the CIO with input from IT department heads

**Item 2.** Which body typically prioritises and approves individual IT projects so that they reflect business priorities, and monitors their delivery?

- A. The IT strategy committee of the board
- B. The IT steering committee
- C. The change advisory board
- D. The information security team

**Item 3.** Which finding about access in a finance system is the GREATEST concern for segregation of duties?

- A. Users in the finance team can view their own team's reports
- B. The database administrator reviews database error logs every week and records the results in a ticket
- C. Developers can move their own code changes into production without independent review
- D. The help desk can reset user passwords after verifying identity

**Item 4.** A small company has only two IT staff, and both need administrator access to every system. Duties cannot be separated. What is the BEST compensating control?

- A. Requiring both staff to take a security course every year
- B. Removing administrator access from one of the two staff and having the other do all administration
- C. Asking both staff to sign the acceptable use policy each year
- D. Independent review by a manager of logs of administrator activity

<details>
<summary>Answers and explanations, items 1 to 4</summary>

**Item 1: A.** The purpose of an IT strategy is to support the business. A plan that does not refer to business objectives cannot show alignment. *Why not D:* drafting by IT is normal; the concern would be if the business did not review and approve it, and the plan's lack of business objectives is the bigger problem. *Why not B:* readability matters, but it is a presentation issue.

**Item 2: B.** The IT steering committee, made up of executives from the business and IT, prioritises and monitors IT investments and projects. *Why not A:* the IT strategy committee works at board level, advising on strategy rather than approving individual projects. *Why not C:* the change advisory board reviews changes, not investments.

**Item 3: C.** Developers moving their own code into production can introduce unauthorised or untested changes with no one else involved. That breaks a key segregation. *Why not D:* password resets after identity verification are a normal help desk task. *Why not B:* reviewing error logs is part of the DBA's job.

**Item 4: D.** When duties cannot be separated, independent review of what privileged users actually did is the standard compensating control. *Why not B:* removing access would leave the company unable to operate. *Why not A:* training helps awareness but does not detect misuse.

</details>

### Set 2

**Item 5.** A company is outsourcing payroll processing to a cloud provider. From the auditor's point of view, which contract term is MOST important?

- A. A right to audit, or a commitment to supply current independent assurance reports
- B. A discount for paying the annual fee in advance
- C. The provider's right to use the company's logo in marketing
- D. Free training sessions for the payroll team whenever the provider releases a new version of the service

**Item 6.** The board states that it will pursue new markets but will not accept more than a moderate level of risk to customer data. What is this statement?

- A. A statement of risk appetite
- B. A measure of residual risk
- C. A measure of inherent risk
- D. A risk register entry

**Item 7.** The CIO wants to report IT's contribution using financial results, user satisfaction, internal process efficiency and staff development. Which tool fits?

- A. A Gantt chart
- B. A risk register
- C. A RACI chart
- D. A balanced scorecard

**Item 8.** Which finding about the information security policy is the GREATEST concern?

- A. It is twenty pages long
- B. It has never been approved by senior management
- C. It was adapted from an industry template published by a professional body
- D. It was last reviewed eleven months ago

<details>
<summary>Answers and explanations, items 5 to 8</summary>

**Item 5: A.** Without a right to audit or independent assurance reports, the company cannot obtain evidence that the provider's controls work, yet it remains accountable for the payroll data. *Why not B:* payment terms are commercial, not a control concern. *Why not D:* training is helpful but does not provide assurance over the provider's controls.

**Item 6: A.** The overall amount and type of risk the board is willing to accept in pursuing its objectives is its risk appetite. *Why not B:* residual risk is what remains after controls, a measurement rather than a statement of willingness. *Why not D:* a register entry records a specific risk, not the board's overall stance.

**Item 7: D.** A balanced scorecard measures performance across financial, customer, internal process and learning and growth perspectives. *Why not A:* a Gantt chart shows project schedules. *Why not C:* a RACI chart shows who is responsible, accountable, consulted and informed.

**Item 8: B.** A policy without senior management approval has no authority, so staff can ignore it without consequence. *Why not D:* an annual review cycle is common, so eleven months is not a concern. *Why not C:* adapting a template is fine if it is tailored and approved.

</details>

### Set 3

**Item 9.** An organisation relies on a service provider's independent assurance report for its hosted HR system. What should the IS auditor check FIRST?

- A. That the provider's security and operations staff hold recognised professional certifications
- B. That the report is written in plain language
- C. That the report's scope covers the services used and its period is current
- D. That the provider has been in business for more than five years

**Item 10.** A new customer relationship system collects customers' national identity numbers, although no business process uses them. What should the IS auditor recommend?

- A. Encrypt the identity numbers in the database
- B. Restrict access to the identity numbers to a small group of managers and log every time they are viewed
- C. Mask the identity numbers on screen
- D. Stop collecting the numbers and remove those already stored, in line with data minimisation

**Item 11.** Who should be responsible for classifying the data held in a sales system?

- A. The IS auditor
- B. The business owner of the sales data
- C. The database administrator
- D. The security administrator

**Item 12.** Which finding in the leavers process is the GREATEST concern?

- A. Exit interviews are held in about half of departures
- B. Leavers return their laptops and badges within a week of leaving rather than on their final day of work
- C. Accounts of several leavers stayed active for weeks, and one was used after the person left
- D. Leavers receive a reminder of their confidentiality obligations by post

<details>
<summary>Answers and explanations, items 9 to 12</summary>

**Item 9: C.** A report is only useful if it covers the services you rely on and a recent period. If it does not, it gives no assurance about your system. *Why not A:* staff certifications say little about whether the specific controls worked. *Why not D:* time in business is a vendor selection factor, not evidence about controls.

**Item 10: D.** Data that no process needs should not be collected. Removing it eliminates the risk rather than reducing it. *Why not A:* encryption protects the data but keeps an unnecessary risk. *Why not C:* masking on screen still leaves the numbers stored.

**Item 11: B.** The data owner, a business manager accountable for the data, classifies it. *Why not C:* the DBA is a custodian who implements the owner's decisions. *Why not A:* the auditor evaluates the classification process and must not make management decisions.

**Item 12: C.** Active accounts after departure, one of them actually used, show the core control has failed and may already have been exploited. *Why not B:* a late laptop return is a weakness, but less serious than live access being used. *Why not A:* exit interviews are useful but not a key control.

</details>

## Score yourself

| Item | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| Answer | A | B | C | D | A | A | D | B | C | D | B | C |

- **11 to 12:** strong governance instincts. Move on to Domains 4 and 5, which carry the most weight.
- **8 to 10:** list which "who decides" questions you missed and redo the committees and roles table.
- **7 or fewer:** reread Key concepts, focusing on governance versus management, risk terms and vendor contracts, then redo the items.

## Next step

Governance items take judgement under time pressure. Practise them with the [free CISA practice test on PrepClubs](https://prepclubs.com/free-practice-tests/cisa?utm_source=github&utm_medium=referral&utm_campaign=study-notes&utm_content=cisa), then return to the traps list.

## Sources for this page

- [ISACA CISA exam content outline](https://www.isaca.org/credentialing/cisa/cisa-exam-content-outline), for the topics and weight

---

<!-- nav:bottom -->← Previous: [Domain 1: Information Systems Auditing Process](information-systems-auditing-process.md) | Next: [Domain 3: Acquisition, Development and Implementation](acquisition-development-and-implementation.md) → | [Back to contents](../../README.md#contents)<!-- /nav:bottom -->
