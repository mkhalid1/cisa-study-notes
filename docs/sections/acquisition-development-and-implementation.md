<!-- nav:top -->
[Contents](../../README.md#contents) · Previous: [Domain 2: Governance and Management of IT](governance-and-management-of-it.md) · Next: [Domain 4: Operations and Business Resilience](operations-and-business-resilience.md)
<!-- /nav:top -->

# Domain 3: Information Systems Acquisition, Development and Implementation

**In one line:** whether new systems are justified, well run as projects, built or bought with the right controls, tested properly and moved into production safely.

ISACA weights this domain at **12%**, the smallest of the five, about 18 questions if the split were exact. It follows a system from idea to go-live and the review afterwards. The auditor's job throughout is to give assurance that the project delivers what was approved, with controls designed in, without the auditor taking over decisions that belong to the project.

## What it covers

| Part A: Information Systems Acquisition and Development (official topics) | What you need to be able to do |
|---|---|
| Project Governance and Management | Assess sponsorship, roles, oversight, planning and tracking. |
| Business Case and Feasibility Analysis | Judge whether the investment was justified and the options compared. |
| System Development Methodologies | Understand waterfall, agile, prototyping, RAD and DevOps and their control implications. |
| Control Identification and Design | Make sure application and security controls are designed in from the start. |

| Part B: Information Systems Implementation (official topics) | What you need to be able to do |
|---|---|
| System Readiness and Implementation Testing | Evaluate test plans, levels of testing and sign-off. |
| Implementation Configuration and Release Management | Check how builds, versions and releases are controlled. |
| System Migration, Infrastructure Deployment, and Data Conversion | Verify data is moved completely and accurately and the cutover is safe. |
| Post-implementation Review | Check whether the system delivers the benefits in the business case. |

## Key concepts

### Project governance

| Role | Responsibility |
|---|---|
| Project sponsor | Senior business owner. Provides funding, owns the business case and the benefits. |
| Steering committee | Oversees the project, approves major changes to scope, budget and timing. |
| Project manager | Plans and runs the project day to day. |
| Project management office | Sets standards and tracks the portfolio. |
| Users and business analysts | Define requirements and accept the system. |
| Quality assurance | Checks that standards and processes are followed. |
| IS auditor | Gives independent assurance and advice on controls, without making project decisions. |

Project management techniques: **work breakdown structure** (break the work into tasks), **Gantt charts** (schedule), **PERT** (estimates using optimistic, most likely and pessimistic times), **critical path method** (the longest chain of dependent tasks; delays on it delay the whole project, and only shortening it shortens the project), **earned value analysis** (compares planned value, earned value and actual cost to show schedule and cost variance), and **timeboxing** (fixed time, flexible scope).

### Business case and feasibility

A business case sets out the problem, options, costs, benefits, risks and how benefits will be measured. Feasibility covers technical, financial, operational and legal angles. Financial measures include return on investment, net present value and payback period. The business case is a living document: it should be revisited at key stages, and if the case no longer holds, the project should be reconsidered.

**Build or buy:** buying off-the-shelf software is usually faster and cheaper but may not fit every requirement. For bought software, **source code escrow** protects the organisation if the vendor fails, by giving it access to the code under agreed conditions.

### Development methodologies

| Method | How it works | Control point |
|---|---|---|
| Waterfall (traditional SDLC) | Sequential phases with sign-off at each | Good documentation and gates; late changes are costly |
| Agile | Short iterations with working software each time | Controls must be built into each iteration, including security and documentation enough for audit |
| Prototyping | Build a model for users to react to | Risk that the prototype becomes production without proper controls |
| Rapid application development | Fast delivery with prototypes and tools | Scope creep and weak documentation |
| DevOps | Development and operations combined, heavy automation | Pipeline controls replace manual gates: automated tests, approvals and segregation in the pipeline |

### Control identification and design

Controls should be specified as requirements and designed in, not added after go-live.

| Application control | Examples |
|---|---|
| Input | **Validity check** (a code exists in the master file), **range check** (value within limits), **limit check** (value does not exceed a limit), **reasonableness check** (value is plausible), **check digit** (a calculated digit that catches transposition and transcription errors), **completeness check** (required fields filled), **duplicate check**, **sequence check** (no gaps or repeats in numbering) |
| Processing | **Batch control totals** (record counts, amount totals, hash totals) compared before and after processing, **run-to-run totals** between processing steps, edit checks, exception reports |
| Output | Reconciliation of output with input totals, controlled distribution, review by users, retention rules |

A **hash total** adds up a field that has no meaning as a sum, such as account numbers, purely to detect changes or missing records.

### Testing

| Test | Purpose | Usually done by |
|---|---|---|
| Unit | Each program or module works | Developers |
| Integration or interface | Modules and systems work together and pass data correctly | Developers and testers |
| System | The whole system meets its specification, including performance and security | Testers |
| Stress or load | Behaviour at or beyond expected volumes | Testers |
| User acceptance (UAT) | The system meets business requirements; users sign off | Users |
| Regression | Changes did not break existing functions | Testers, often automated |
| Pilot | A limited live trial with a group of users or a site | Business and IT |

Test in a separate environment with test data that is realistic. If production data is used for testing, it must be protected or masked. Testing evidence and sign-off are what the auditor looks for before go-live.

### Configuration and release management

Keep development, test and production environments separate. Control versions of code and configuration, so you know exactly what is running. Releases follow change management: approval, testing, scheduled deployment, back-out plan and documentation. Developers should not move their own code into production. Emergency releases follow a faster path but are still documented and approved afterwards.

### Migration and data conversion

Data conversion controls make sure data is **complete, accurate and authorised** after the move:

- record counts, control totals and hash totals compared between old and new systems
- reconciliation of balances and exception reports
- data cleansing before migration, with approval of what is changed
- an audit trail of the conversion
- user sign-off of converted data
- a back-out plan, with the old system kept available until the new one is accepted

| Changeover method | How it works | Risk |
|---|---|---|
| Parallel | Old and new run side by side; results compared | Lowest risk, highest cost and effort |
| Phased | The new system replaces the old in stages, by module or function | Moderate; interfaces between old and new parts are complex |
| Pilot | One site or group goes live first | Moderate; problems are contained to the pilot |
| Direct (abrupt, big bang) | Old system switched off, new one switched on | Highest risk; no fallback if the new system fails |

### Post-implementation review

A post-implementation review (PIR) checks whether the system meets requirements, whether controls work, and whether the **benefits in the business case** are being realised. It is most useful after the system has stabilised, often some months after go-live, when results can be measured. It should be done by someone independent of the project, and lessons learned feed into future projects.

### The auditor in a project

The auditor can review the business case, project controls, test results and conversion, and advise on control requirements. To stay independent, the auditor should not design controls, write the test scripts the project relies on, or approve go-live. Those decisions belong to management.

## How the questions look

Expect project scenarios: a business case, a schedule slip, a test plan, a data migration, a go-live decision, a PIR. Questions ask what the auditor should check FIRST, what is the GREATEST risk, which test or control fits, or which changeover method suits the risk. Many turn on the auditor staying in an assurance role.

## A method that works

1. **Locate the project stage.** Business case, design, build, test, migrate, go-live or review.
2. **Ask whether the project still delivers the approved benefits.** The business case is the yardstick from start to finish.
3. **For controls, ask whether they were designed in.** Input, processing and output controls are requirements, not afterthoughts.
4. **For testing, find who must sign off.** Users accept business functionality; technical tests come first.
5. **For migration, look for completeness and accuracy evidence.** Counts, totals and reconciliations.
6. **Keep your role.** Advise and assure; do not design, build or approve.

## Traps that cost points

- **Letting the auditor design or approve.** It impairs independence.
- **Skipping UAT because system testing passed.** System tests check the specification; UAT checks business needs.
- **Treating a direct cutover as low risk for a critical system.** It has no fallback.
- **Accepting migration without reconciliation.** Counts and totals are the evidence.
- **Running the PIR on day one.** Benefits cannot be measured until the system has stabilised.
- **Confusing check digits with range checks.** Check digits catch transposition and transcription errors in codes.
- **Ignoring escrow for a critical bought system.** If the vendor fails, you may be left with software no one can maintain.
- **Using unmasked production data for testing.** It exposes real personal data outside production controls.

## Timing

As guidance, Domain 3 items take 60 to 80 seconds. Control-type questions (which check fits) are quicker; project judgement questions take longer.

## Practice items

These 4 items are original, written for these notes. They are not taken from ISACA or any prep provider.

### Set 1

**Item 1.** During a post-implementation review of a new ordering system, what should the IS auditor compare FIRST?

- A. The benefits actually achieved against those in the approved business case
- B. The number of help desk calls in the first week against the numbers for other recently launched systems
- C. The final project cost against the original vendor quotation only
- D. The number of features delivered against the original wish list

**Item 2.** Customer records are being migrated from an old billing system to a new one. Which is the BEST evidence that the data was converted completely and accurately?

- A. The vendor's statement that the migration tool is reliable
- B. Users' comments that the new screens look correct
- C. The project manager's formal sign-off confirming that the migration finished on time and within budget
- D. Reconciliation of record counts and control totals between the old and new systems

**Item 3.** A bank is replacing its core payments system. All branches share one ledger, so the system cannot be switched over branch by branch or module by module. A failure at go-live would be severe, and the bank can afford extra effort to reduce that risk. Which changeover method fits BEST?

- A. Direct cutover over a weekend
- B. Phased replacement by module over several months, starting with the least critical functions
- C. Pilot at one branch
- D. Parallel running of old and new systems with comparison of results

**Item 4.** An IS auditor reviews emergency changes made to production during a system's first month. Which finding is the GREATEST concern?

- A. Emergency changes were not reviewed and approved after they were made
- B. Most emergency changes were made outside business hours
- C. Emergency changes were made only by a small group of named, authorised support staff on the on-call rota
- D. A log is kept of every emergency change

<details>
<summary>Answers and explanations, items 1 to 4</summary>

**Item 1: A.** A post-implementation review checks whether the system delivers the benefits that justified it, so the approved business case is the yardstick. *Why not C:* the vendor quote is only part of the cost and says nothing about benefits. *Why not D:* a wish list is not the approved scope or the measure of value.

**Item 2: D.** Counts and control totals reconciled between source and target are direct evidence of completeness and accuracy. *Why not B:* screens that look right do not show that every record arrived with correct values. *Why not C:* finishing on time says nothing about data quality.

**Item 3: D.** Parallel running keeps the old system live while results are compared, so problems are found without disrupting payments. It costs more but gives the most assurance. *Why not C:* a pilot needs part of the organisation to go live on its own, which a single shared ledger rules out. *Why not B:* phasing by module is ruled out for the same reason. *Why not A:* a direct cutover has no fallback at all.

**Item 4: A.** Emergency changes skip some steps before implementation, so retrospective review and approval is the control that keeps them accountable. Without it, unauthorised changes can go unnoticed. *Why not B:* working outside hours is normal for emergency fixes. *Why not C:* changes made by authorised staff are what you want to see.

</details>

Want more? The [free timed CISA practice test on PrepClubs](https://prepclubs.com/free-practice-tests/cisa?utm_source=github&utm_medium=referral&utm_campaign=study-notes&utm_content=cisa) has 25 questions across all five domains, with your score broken down by domain.

## Score yourself

| Item | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Answer | A | D | D | A |

- **4:** strong. Domain 3 is the smallest, so move your time to Domains 4 and 5.
- **3:** check whether misses were about controls and tests (learn the tables) or the auditor's role.
- **2 or fewer:** reread the application controls, testing and changeover tables, then redo the items.

## Next step

Practise project and control items in a timed set with the [free CISA practice test on PrepClubs](https://prepclubs.com/free-practice-tests/cisa?utm_source=github&utm_medium=referral&utm_campaign=study-notes&utm_content=cisa), then return to the traps list.

## Sources for this page

- [ISACA CISA exam content outline](https://www.isaca.org/credentialing/cisa/cisa-exam-content-outline), for the topics and weight

---

<!-- nav:bottom -->
← Previous: [Domain 2: Governance and Management of IT](governance-and-management-of-it.md) | Next: [Domain 4: Operations and Business Resilience](operations-and-business-resilience.md) → | [Back to contents](../../README.md#contents)
<!-- /nav:bottom -->
