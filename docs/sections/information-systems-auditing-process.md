<!-- nav:top -->
[Contents](../../README.md#contents) · Previous: [5-minute diagnostic](../diagnostic.md) · Next: [Domain 2: Governance and Management of IT](governance-and-management-of-it.md)
<!-- /nav:top -->

# Domain 1: Information Systems Auditing Process

**In one line:** how an IS audit is planned, carried out, evidenced and reported, and how the auditor stays independent while doing it.

ISACA weights this domain at **18%** of the exam, about 27 of the 150 questions if the split were exact. It is the method behind every other domain. When a question in Domain 4 or 5 asks what the auditor should do FIRST, the answer usually comes from this chapter: understand the risk, gather sufficient evidence, report rather than fix, and follow up.

## What it covers

ISACA splits the domain into two parts.

| Part A: Planning (official topics) | What you need to be able to do |
|---|---|
| IS Audit Standards, Guidelines, and Codes of Ethics | Apply ISACA's audit standards and Code of Professional Ethics to real situations. |
| Types of Audits, Assessments, and Reviews | Tell compliance, financial, operational, integrated, forensic and specialised work apart, and know when an assessment is not an audit. |
| Risk-Based Audit Planning | Use risk to decide what to audit, when and how deeply. |
| Types of Controls and Considerations | Classify controls and judge whether they address the risk. |

| Part B: Execution (official topics) | What you need to be able to do |
|---|---|
| Audit Project Management | Run an engagement from charter and scope to fieldwork and reporting. |
| Audit Testing and Sampling Methodology | Choose compliance or substantive testing and the right sampling method. |
| Audit Evidence Collection Techniques | Gather sufficient, reliable, relevant evidence. |
| Audit Data Analytics | Use CAATs, data analytics and continuous auditing techniques. |
| Reporting and Communication Techniques | Write findings management can act on, and communicate them well. |
| Quality Assurance and Improvement of Audit Process | Review and improve the audit function itself. |

## Key concepts

### Authority, standards and ethics

- **Audit charter:** approved by the board or audit committee, it sets the internal audit function's purpose, authority, responsibility and accountability. It is the source of the auditor's right to access records and people.
- **Engagement letter:** used mainly for external or specific engagements, it sets the scope, objectives and responsibilities for one assignment.
- **ISACA's IT Audit Framework (ITAF)** contains standards, which are mandatory for CISAs, guidelines that help apply them, and tools and techniques. In our own words, the standards cover the charter, independence, due professional care, proficiency, planning, evidence, reporting and follow-up.
- **Independence and objectivity:** the auditor must be free, in fact and in appearance, from anything that would bias judgement. Auditing a system you designed, implemented or run impairs independence. If independence is impaired, disclose it to the appropriate parties before or during the work.
- **Code of Professional Ethics:** every CISA agrees to it, including due care, confidentiality, competence and informing appropriate parties of the results of work.

### Types of audits and reviews

| Type | Focus |
|---|---|
| Compliance | Whether specific rules, policies or regulations are followed |
| Financial | Whether financial information is fairly stated |
| Operational | Whether operations are efficient and effective |
| Integrated | Financial, operational and IS aspects together |
| IS audit | Whether IS controls safeguard assets, keep data accurate and support objectives |
| Forensic | Collecting and analysing evidence for possible legal action, usually after suspected fraud |
| Specialised | Specific areas, such as a third-party service review |
| Control self-assessment (CSA) | Management and staff assess their own controls, often in workshops; the auditor facilitates. It complements audit but does not replace it. |

### Risk-based audit planning

1. Understand the business, its objectives and its processes.
2. Identify the **audit universe** and assess risk in each area.
3. Build the audit plan around the highest risks, agreed with the audit committee.
4. For each engagement, plan scope and approach around the key risks and controls.

**Audit risk** is the risk that the auditor reaches the wrong conclusion. It has three parts:

| Component | Meaning | Who can change it |
|---|---|---|
| Inherent risk | Risk of material error before any controls | Nobody, it is a property of the area |
| Control risk | Risk that controls fail to prevent or detect the error | Management, through better controls |
| Detection risk | Risk that the auditor's procedures miss the error | The auditor, through the nature, timing and extent of testing |

Audit risk = inherent risk x control risk x detection risk. When inherent and control risk are high, the auditor must lower detection risk with more and stronger testing.

**Materiality** in IS audit is about whether an error or weakness could matter to decisions or objectives, whatever its money value. A weak control over a small system can be material if that system feeds financial reporting.

### Types of controls

- By function: **preventive** (stop it happening), **detective** (find it), **corrective** (fix it), plus deterrent, directive, recovery and compensating.
- By nature: manual or automated; general IT controls (access, change management, operations) or application controls (input, processing, output).
- **Compensating controls** reduce risk when the ideal control is not feasible, for example supervisory review where duties cannot be separated.
- General IT controls underpin application controls: if change management fails, you cannot rely on an automated control staying as designed.

### Audit testing and sampling

| | Compliance testing | Substantive testing |
|---|---|---|
| Question | Does the control work as designed? | Is the data or balance correct? |
| Example | Do change tickets have approval before implementation? | Is the inventory quantity correct? |
| Typical sampling | Attribute sampling | Variable sampling |

| Sampling method | Use |
|---|---|
| Statistical | Random selection and probability let you quantify confidence and project results |
| Non-statistical (judgemental) | Auditor chooses items using judgement; results cannot be projected statistically |
| Attribute | Estimates the rate of occurrence of a characteristic, such as missing approvals |
| Variable | Estimates a monetary or quantity value, such as total overstatement |
| Stop-or-go | Attribute sampling that stops early if few or no errors are found; used when few errors are expected |
| Discovery | Designed to find at least one instance when the rate is expected to be very low, such as fraud |
| Stratified | Divides the population into groups, such as by value, and samples each |

Key terms: **confidence coefficient** (how sure you want to be; higher means a larger sample), **tolerable error** (the most error you can accept; lower means a larger sample), **expected error** (higher means a larger sample), **precision** (how close the sample result is to the population).

### Evidence

Evidence must be **sufficient** (enough), **reliable**, **relevant** and **useful**. In general, evidence is more reliable when it is:

- obtained from an independent source outside the auditee, such as a bank confirmation sent directly to the auditor
- obtained directly by the auditor, through observation, inspection, recalculation or reperformance
- documented rather than oral
- original rather than a copy
- produced by a system with effective controls

Collection techniques: inquiry (weakest on its own), observation, inspection of documents and records, walkthroughs, reperformance, recalculation, and analytical review.

### Data analytics and CAATs

Computer-assisted audit techniques let you test entire populations instead of samples: generalised audit software for extraction, sorting and matching, and scripts for analytics such as duplicate payments, gaps in sequences or unusual times.

| Continuous auditing technique | How it works |
|---|---|
| Integrated test facility (ITF) | A dummy entity is set up in the live system and test transactions are processed alongside real ones |
| Embedded audit module or SCARF | Audit code built into the application captures transactions that meet set criteria for later review |
| Snapshot | Records the state of a transaction at points as it moves through processing |
| Audit hooks | Flags in the application that alert the auditor when suspicious transactions occur |
| Continuous and intermittent simulation (CIS) | Simulates processing of selected transactions alongside the live run |
| Parallel simulation | The auditor reprocesses real data with their own program and compares results |

### Reporting and follow-up

- A finding usually contains **condition** (what is), **criteria** (what should be), **cause**, **effect** (the risk) and a **recommendation**.
- Discuss findings with management before the report is final, at an exit meeting, to confirm facts and get management responses.
- If management disagrees, the auditor checks the evidence again; if it holds, the finding stays in the report alongside management's response.
- The report goes to the audience defined in the charter, typically the audit committee and senior management.
- **Management** is responsible for implementing fixes. The **auditor follows up** to confirm actions were taken and work as intended. The auditor does not implement fixes.

### Quality assurance

Audit functions maintain quality through supervision and review of working papers, internal quality reviews, and periodic external assessments. Lessons from each engagement improve the audit process.

## How the questions look

ISACA's item writing guide describes CISA items as multiple choice with a stem and four options: one key and three distractors. The key reflects current practice and is sometimes the only correct option and sometimes the BEST of those offered. ISACA writes for the minimally competent candidate with three to five years of experience, and avoids negative wording such as NOT or LEAST, true or false items and pure definition questions.

So expect short scenarios: "An IS auditor is planning...", "During fieldwork the auditor discovers...", "Which evidence would be MOST reliable?", "What should the auditor do FIRST?" Read them as an auditor, not as the manager or the engineer.

## A method that works

1. **Find your role.** You are the IS auditor. You plan, test, evaluate and report. You do not design, implement or approve controls.
2. **Find the stage.** Planning, fieldwork, reporting or follow-up? The right action belongs to the current stage.
3. **Look for risk first.** In planning questions, a risk assessment or understanding of the area usually comes before choosing tests.
4. **Weigh the evidence.** Prefer independent, direct, documented, original evidence.
5. **Match the test to the question.** Is the control working (compliance)? Is the data right (substantive)? Rate of error (attribute) or value (variable)?
6. **When you find a problem, report it.** Gather evidence, discuss with management, report, follow up.

## Traps that cost points

- **Fixing the problem yourself.** Auditors recommend; management fixes.
- **Accepting an auditee's word as enough.** Inquiry alone is weak evidence. Corroborate it.
- **Dropping a finding because management disagrees.** Recheck the evidence, then report the finding with management's response.
- **Choosing variable sampling for a control test.** Control tests use attribute sampling.
- **Using discovery sampling to estimate an error rate.** It is for finding at least one occurrence.
- **Treating control self-assessment as a replacement for audit.** It complements audit.
- **Ignoring independence.** If you helped design it, disclose the impairment.
- **Starting fieldwork before planning.** Understand the area and its risks first.
- **Thinking detection risk is the auditee's problem.** It is the one component the auditor controls.

## Timing

The exam gives 4 hours for 150 questions, an average of 96 seconds each. As guidance, most Domain 1 items take 60 to 80 seconds. If two options both seem right, ask which one an auditor would do and which one management would do; the auditor's action is usually the answer.

## Practice items

These 4 items are original, written for these notes. They are not taken from ISACA, its review materials or any prep provider.

### Set 1

**Item 1.** An IS auditor is assigned to audit the company's new cloud-based procurement process. What should the auditor do FIRST?

- A. Gain an understanding of the process and assess its risks
- B. Select a statistical sample of purchase orders to test
- C. Write detailed test steps for each control the auditor expects to find
- D. Agree a date with the auditee for the closing meeting

**Item 2.** An IS auditor suspects that a few fictitious vendors may have been created in the payables system. The expected rate is very low, and the goal is to find at least one if any exist. Which sampling method fits BEST?

- A. Variable sampling
- B. Stop-or-go sampling
- C. Judgemental sampling
- D. Discovery sampling

**Item 3.** An IS auditor is verifying the year-end balance of a bank account. Which evidence is MOST reliable?

- A. A bank statement printed by the company's accountant
- B. A confirmation sent by the bank directly to the auditor
- C. A statement from the finance manager that the balance is correct
- D. An email from the accountant forwarding the bank's balance figure

**Item 4.** The IT director asks an IS auditor to help design the access controls for a new system that the same auditor is scheduled to audit next quarter. What is the BEST response?

- A. Agree, since the auditor's knowledge will improve the controls
- B. Agree, but not mention it in the later audit report
- C. Decline any contact with the project, and refuse to answer the team's questions until the audit is complete
- D. Offer to advise on control requirements without designing the controls, and disclose the potential impairment to the audit committee

<details>
<summary>Answers and explanations, items 1 to 4</summary>

**Item 1: A.** Planning starts with understanding the process and its risks, which then drives scope, tests and sampling. *Why not C:* writing test steps before understanding the process risks testing the wrong things. *Why not B:* choosing a sample comes after the test approach is designed.

**Item 2: D.** Discovery sampling is designed to find at least one occurrence when the expected rate is very low, which suits suspected fraud. *Why not B:* stop-or-go sampling helps conclude a control works when few errors are expected; it is not built to find a rare instance. *Why not C:* judgemental selection cannot give a measured chance of finding a rare item.

**Item 3: B.** Evidence from an independent source, sent directly to the auditor, is the most reliable. *Why not A:* a document that passes through the auditee's hands could be altered. *Why not D:* a forwarded email also passes through the auditee and is a copy.

**Item 4: D.** Designing controls you will later audit impairs independence. The auditor can still add value by advising on what the controls must achieve, leaving the design to management and disclosing the potential impairment. *Why not A:* better controls do not cure the independence problem. *Why not C:* a complete refusal is not required; auditors can advise without making design decisions.

</details>

Want more? The [free timed CISA practice test on PrepClubs](https://prepclubs.com/free-practice-tests/cisa?utm_source=github&utm_medium=referral&utm_campaign=6n8cun&utm_content=cisa) has 25 questions across all five domains, with your score broken down by domain.

## Score yourself

| Item | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Answer | A | D | B | D |

- **4:** strong. This thinking carries into every other domain.
- **3:** look at whether misses were about sampling and techniques (learn the tables) or about the auditor's role (reread the method, step 1).
- **2 or fewer:** reread Key concepts, then explain the audit risk model and the sampling table out loud from memory before redoing the items.

## Next step

Auditor judgement improves fastest with volume against a clock. Try the [free CISA practice test on PrepClubs](https://prepclubs.com/free-practice-tests/cisa?utm_source=github&utm_medium=referral&utm_campaign=6n8cun&utm_content=cisa), then come back to the traps list for anything you missed.

## Sources for this page

- [ISACA CISA exam content outline](https://www.isaca.org/credentialing/cisa/cisa-exam-content-outline), for the topics and weight
- [ISACA CISA Item Development Guide (PDF, updated October 2018)](https://www.isaca.org/certifications/additional-resources/-/media/487125b6c4e14a638c3f52ca3f8af344.ashx), for how items are written

---

<!-- nav:bottom -->
← Previous: [5-minute diagnostic](../diagnostic.md) | Next: [Domain 2: Governance and Management of IT](governance-and-management-of-it.md) → | [Back to contents](../../README.md#contents)
<!-- /nav:bottom -->
