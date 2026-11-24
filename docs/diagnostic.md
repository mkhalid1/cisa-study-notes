<!-- nav:top -->[Contents](../README.md#contents) · Previous: [The CISA exam explained](test-overview.md) · Next: [Domain 1: Information Systems Auditing Process](sections/information-systems-auditing-process.md)<!-- /nav:top -->

# 15-minute diagnostic

Fifteen short, original items, three from each domain, to show you where to start. Set a timer for 15 minutes, answer everything without looking anything up, then check each part and read the table at the bottom.

These items are original, written for these notes. They are not taken from ISACA or any prep provider. They are shorter and more direct than real CISA items, because the goal is to find gaps quickly. The domain guides have longer, exam-style scenarios.

If you already know your weak areas, skip this and take the [free CISA practice test on PrepClubs](https://prepclubs.com/free-practice-tests/cisa?utm_source=github&utm_medium=referral&utm_campaign=study-notes&utm_content=cisa) for a timed, mixed set instead.

## Part A: Information Systems Auditing Process

**D1.** Which evidence is MOST reliable?

- A. The auditor's own recalculation of an interest charge
- B. A manager's verbal explanation of how interest is calculated
- C. A photocopy of a calculation provided by the auditee
- D. A draft email from the finance team describing the calculation

**D2.** Testing whether a control operated as designed is called:

- A. a substantive test.
- B. a compliance test.
- C. an analytical review.
- D. a walkthrough.

**D3.** Who should approve the internal audit charter?

- A. The CIO
- B. The CFO
- C. The audit committee or board
- D. The external auditor

<details>
<summary>Answers, part A</summary>

**D1: A.** Evidence the auditor obtains directly, such as a recalculation, is more reliable than evidence supplied or described by the auditee.

**D2: B.** Compliance tests check that controls work. Substantive tests check that data and balances are correct.

**D3: C.** The charter sets audit's authority, so it is approved at the top, by the audit committee or board, not by management the audit may examine.

</details>

## Part B: Governance and Management of IT

**D4.** The IT strategy should be derived mainly from:

- A. vendors' product roadmaps.
- B. the business strategy.
- C. last year's IT budget.
- D. general industry technology trends.

**D5.** When a business process is outsourced, who remains accountable for it?

- A. The organisation that outsourced it
- B. The service provider
- C. The regulator
- D. The insurer

**D6.** Which pair of duties is MOST important to give to different people?

- A. Viewing a report and printing it
- B. Resetting passwords and unlocking accounts
- C. Running backups and checking the backup logs
- D. Initiating a payment and approving the same payment

<details>
<summary>Answers, part B</summary>

**D4: B.** IT strategy exists to support the business strategy and should be derived from it.

**D5: A.** You can outsource the activity but not the accountability.

**D6: D.** If one person can both initiate and approve a payment, they can pay themselves. The other pairs carry little fraud risk.

</details>

## Part C: Acquisition, Development and Implementation

**D7.** Which changeover method carries the highest risk?

- A. Parallel running
- B. Pilot
- C. Phased
- D. Direct cutover

**D8.** Which testing checks that separate modules pass data to each other correctly?

- A. Unit testing
- B. User acceptance testing
- C. Integration testing
- D. Regression testing

**D9.** A hash total is:

- A. a sum of a field that has no meaning as a total, used to detect missing or changed records.
- B. the total value of all transactions in a batch.
- C. an encrypted copy of a file used for backup.
- D. the number of records in a file.

<details>
<summary>Answers, part C</summary>

**D7: D.** A direct cutover switches off the old system with no fallback.

**D8: C.** Integration, or interface, testing checks how modules work together. Unit testing checks each module alone.

**D9: A.** For example, adding up account numbers. The sum means nothing, but if it changes, records were lost or altered. A value total (B) and a record count (D) are different control totals.

</details>

## Part D: Operations and Business Resilience

**D10.** A full backup runs on Sunday night and incremental backups run on Monday to Saturday nights. To restore after a failure on Thursday morning, you need:

- A. Sunday's full backup and the incrementals from Monday, Tuesday and Wednesday.
- B. Sunday's full backup only.
- C. Wednesday's incremental only.
- D. Sunday's full backup and Wednesday's incremental only.

**D11.** The recovery point objective is:

- A. the time allowed to restore a system.
- B. the maximum acceptable data loss, measured in time.
- C. the longest outage the business can tolerate.
- D. the level of service needed during recovery.

**D12.** Which agreement is made between IT and an external supplier that supports a service IT provides?

- A. A service level agreement
- B. An operational level agreement
- C. An underpinning contract
- D. A non-disclosure agreement

<details>
<summary>Answers, part D</summary>

**D10: A.** Each incremental holds only the changes since the previous backup, so you need the full and every incremental since.

**D11: B.** RPO is about data loss. Time to restore is the RTO.

**D12: C.** An underpinning contract is with an external supplier. An SLA is with the business; an OLA is between internal IT teams.

</details>

## Part E: Protection of Information Assets

**D13.** Which type of firewall tracks connections and allows only traffic that belongs to a permitted session?

- A. A packet-filtering firewall
- B. An application-level proxy
- C. A web application firewall
- D. A stateful firewall

**D14.** To send a file that only one recipient can read, you encrypt it, or the session key protecting it, with:

- A. your own private key.
- B. the recipient's public key.
- C. the recipient's private key.
- D. your own public key.

**D15.** Unusually low humidity in a server room mainly increases the risk of:

- A. condensation on equipment.
- B. corrosion of circuit boards.
- C. static electricity damaging components.
- D. water leaks.

<details>
<summary>Answers, part E</summary>

**D13: D.** A stateful firewall keeps a table of connections. A packet filter judges each packet alone, without context.

**D14: B.** Only the recipient's private key can decrypt it. Signing, by contrast, uses your own private key.

**D15: C.** Dry air lets static build up. Condensation and corrosion are risks of high humidity.

</details>

## What your result means

Count your correct answers in each part.

| Part | Your score | If you scored 0 or 1 | If you scored 2 | If you scored 3 |
|---|---|---|---|---|
| A. Auditing process | /3 | Start with [Domain 1](sections/information-systems-auditing-process.md) | Relearn evidence and sampling | Light review only |
| B. Governance | /3 | Start with [Domain 2](sections/governance-and-management-of-it.md) | Relearn roles, risk terms and vendor controls | Light review only |
| C. Acquisition and development | /3 | Start with [Domain 3](sections/acquisition-development-and-implementation.md) | Relearn testing, controls and changeover | Light review only |
| D. Operations and resilience | /3 | Start with [Domain 4](sections/operations-and-business-resilience.md) | Relearn backups, recovery terms and sites | Light review only |
| E. Protection of assets | /3 | Start with [Domain 5](sections/protection-of-information-assets.md) | Relearn access, network and cloud controls | Light review only |

Domains 4 and 5 carry 52% of the exam between them, so if they are close to your other scores, start there. Then pick a plan: the [7-day plan](study-plans.md#7-day-plan) for your final week, or the [2-day plan](study-plans.md#2-day-plan) if the exam is close.

---

<!-- nav:bottom -->← Previous: [The CISA exam explained](test-overview.md) | Next: [Domain 1: Information Systems Auditing Process](sections/information-systems-auditing-process.md) → | [Back to contents](../README.md#contents)<!-- /nav:bottom -->
