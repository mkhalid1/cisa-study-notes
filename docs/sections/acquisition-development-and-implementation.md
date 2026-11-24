<!-- nav:top -->[Contents](../../README.md#contents) · Previous: [Domain 2: Governance and Management of IT](governance-and-management-of-it.md) · Next: [Domain 4: Operations and Business Resilience](operations-and-business-resilience.md)<!-- /nav:top -->

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

These 12 items are original, written for these notes. They are not taken from ISACA or any prep provider.

### Set 1

**Item 1.** During a post-implementation review of a new ordering system, what should the IS auditor compare FIRST?

- A. The benefits actually achieved against those in the approved business case
- B. The number of help desk calls in the first week against the numbers for other recently launched systems
- C. The final project cost against the original vendor quotation only
- D. The number of features delivered against the original wish list

**Item 2.** A project is behind schedule. The sponsor asks which tasks should receive extra resources to bring the end date forward. Which tasks should they be?

- A. Tasks with the most slack in the schedule
- B. Tasks on the critical path
- C. The tasks with the lowest cost
- D. The tasks scheduled to start first

**Item 3.** Clerks often swap two digits when keying customer account numbers. Which input control would detect this BEST?

- A. A range check
- B. A limit check
- C. A check digit
- D. A reasonableness check

**Item 4.** Customer records are being migrated from an old billing system to a new one. Which is the BEST evidence that the data was converted completely and accurately?

- A. The vendor's statement that the migration tool is reliable
- B. Users' comments that the new screens look correct
- C. The project manager's formal sign-off confirming that the migration finished on time and within budget
- D. Reconciliation of record counts and control totals between the old and new systems

<details>
<summary>Answers and explanations, items 1 to 4</summary>

**Item 1: A.** A post-implementation review checks whether the system delivers the benefits that justified it, so the approved business case is the yardstick. *Why not C:* the vendor quote is only part of the cost and says nothing about benefits. *Why not D:* a wish list is not the approved scope or the measure of value.

**Item 2: B.** The critical path is the longest chain of dependent tasks. Only shortening it can bring the end date forward. *Why not A:* tasks with slack can slip without affecting the end date, so speeding them up gains nothing. *Why not D:* early tasks are not necessarily on the critical path.

**Item 3: C.** A check digit is calculated from the other digits, so swapped or mistyped digits produce a mismatch. *Why not A:* a range check confirms a value falls between limits, and a transposed account number may still fall in range. *Why not D:* a reasonableness check tests whether a value is plausible, not whether a code was keyed correctly.

**Item 4: D.** Counts and control totals reconciled between source and target are direct evidence of completeness and accuracy. *Why not B:* screens that look right do not show that every record arrived with correct values. *Why not C:* finishing on time says nothing about data quality.

</details>

### Set 2

**Item 5.** A bank is replacing its core payments system. All branches share one ledger, so the system cannot be switched over branch by branch or module by module. A failure at go-live would be severe, and the bank can afford extra effort to reduce that risk. Which changeover method fits BEST?

- A. Direct cutover over a weekend
- B. Phased replacement by module over several months, starting with the least critical functions
- C. Pilot at one branch
- D. Parallel running of old and new systems with comparison of results

**Item 6.** Which testing BEST confirms that a new system meets the business's requirements before go-live?

- A. User acceptance testing
- B. Unit testing
- C. Stress testing
- D. Regression testing

**Item 7.** An IS auditor is invited to join the project team for a new ERP system. Which role BEST preserves the auditor's independence?

- A. Designing the user access matrix for the new system
- B. Advising on control requirements and reviewing the design, while leaving decisions to management
- C. Approving the go-live decision on behalf of internal audit
- D. Writing and executing the user acceptance test scripts so that testing reflects audit's view of the controls

**Item 8.** A company buys a critical, customised system from a small vendor. The company is worried about being unable to maintain the software if the vendor goes out of business. Which arrangement addresses this BEST?

- A. A service level agreement with penalties for downtime
- B. A non-disclosure agreement covering the company's data
- C. A source code escrow agreement
- D. A licence audit clause

<details>
<summary>Answers and explanations, items 5 to 8</summary>

**Item 5: D.** Parallel running keeps the old system live while results are compared, so problems are found without disrupting payments. It costs more but gives the most assurance. *Why not C:* a pilot needs part of the organisation to go live on its own, which a single shared ledger rules out. *Why not B:* phasing by module is ruled out for the same reason. *Why not A:* a direct cutover has no fallback at all.

**Item 6: A.** UAT is where users confirm the system does what the business needs, and they sign off. *Why not D:* regression testing checks that changes did not break existing functions, not that the system meets business needs. *Why not B:* unit tests check individual modules against the technical specification.

**Item 7: B.** The auditor can advise and review while management keeps the decisions, which preserves independence. *Why not A:* designing the access matrix is a management control decision the auditor would later have to audit. *Why not C:* approving go-live is a management decision.

**Item 8: C.** Escrow places the source code with a third party, to be released to the company under agreed conditions such as vendor failure. *Why not A:* an SLA is worthless if the vendor no longer exists. *Why not D:* a licence audit clause lets the vendor check the company's usage; it does not protect the company.

</details>

### Set 3

**Item 9.** An IS auditor reviews emergency changes made to production during a system's first month. Which finding is the GREATEST concern?

- A. Emergency changes were not reviewed and approved after they were made
- B. Most emergency changes were made outside business hours
- C. Emergency changes were made only by a small group of named, authorised support staff on the on-call rota
- D. A log is kept of every emergency change

**Item 10.** After a fix to the invoicing module, the team re-runs a suite of earlier tests to make sure other functions still work. What is this?

- A. Unit testing
- B. User acceptance testing
- C. Pilot testing
- D. Regression testing

**Item 11.** When is a post-implementation review usually MOST effective?

- A. During system design
- B. On the day of go-live, while the project team is still together
- C. Once the system has stabilised and its benefits can be measured
- D. Before user acceptance testing

**Item 12.** Which control BEST detects that transactions were lost between batch entry and the master file update?

- A. Password controls and session timeouts on the data entry screens used by clerks
- B. Comparing batch control totals before and after processing
- C. A check digit on customer numbers
- D. A distribution list for output reports

<details>
<summary>Answers and explanations, items 9 to 12</summary>

**Item 9: A.** Emergency changes skip some steps before implementation, so retrospective review and approval is the control that keeps them accountable. Without it, unauthorised changes can go unnoticed. *Why not B:* working outside hours is normal for emergency fixes. *Why not C:* changes made by authorised staff are what you want to see.

**Item 10: D.** Re-running earlier tests to check that a change did not break existing functions is regression testing. *Why not A:* unit testing checks a single module, usually the changed one, rather than re-checking the rest. *Why not B:* UAT is the users' check that business requirements are met.

**Item 11: C.** Benefits and control effectiveness can only be measured once the system is in steady use. *Why not B:* on go-live day there is no performance data yet. *Why not A:* a review during design is a design review, not a post-implementation review.

**Item 12: B.** Batch control totals, such as record counts and amount totals, compared before and after processing reveal lost or added transactions. *Why not C:* a check digit catches keying errors in a field, not missing records. *Why not D:* a distribution list controls who receives output, after processing.

</details>

## Score yourself

| Item | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| Answer | A | B | C | D | D | A | B | C | A | D | C | B |

- **11 to 12:** strong. Domain 3 is the smallest, so move your time to Domains 4 and 5.
- **8 to 10:** check whether misses were about controls and tests (learn the tables) or the auditor's role.
- **7 or fewer:** reread the application controls, testing and changeover tables, then redo the items.

## Next step

Practise project and control items in a timed set with the [free CISA practice test on PrepClubs](https://prepclubs.com/free-practice-tests/cisa?utm_source=github&utm_medium=referral&utm_campaign=study-notes&utm_content=cisa), then return to the traps list.

## Sources for this page

- [ISACA CISA exam content outline](https://www.isaca.org/credentialing/cisa/cisa-exam-content-outline), for the topics and weight

---

<!-- nav:bottom -->← Previous: [Domain 2: Governance and Management of IT](governance-and-management-of-it.md) | Next: [Domain 4: Operations and Business Resilience](operations-and-business-resilience.md) → | [Back to contents](../../README.md#contents)<!-- /nav:bottom -->
