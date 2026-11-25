<!-- nav:top -->
[Contents](../../README.md#contents) · Previous: [Domain 3: Acquisition, Development and Implementation](acquisition-development-and-implementation.md) · Next: [Domain 5: Protection of Information Assets](protection-of-information-assets.md)
<!-- /nav:top -->

# Domain 4: Information Systems Operations and Business Resilience

**In one line:** whether IT runs reliably day to day, changes safely, and can recover when something goes badly wrong.

ISACA weights this domain at **26%**, joint largest with Domain 5, about 39 questions if the split were exact. It is the widest domain in topics: everything from job scheduling and spreadsheets to backups and disaster recovery sites. Because of its weight, this guide has 16 practice items instead of 12.

## What it covers

| Part A: Information Systems Operations (official topics) | What you need to be able to do |
|---|---|
| IT Components | Know the hardware, software, network and middleware an organisation runs on. |
| IT Asset Management | Check assets are inventoried, owned, licensed and tracked through their life. |
| Job Scheduling and Production Process Automation | Assess control over scheduled jobs and automated processes. |
| System Interfaces | Verify data passes between systems completely and accurately. |
| Shadow IT and End-User Computing | Assess risks of unapproved tools and user-built applications such as spreadsheets. |
| Systems Availability and Capacity Management | Check systems are monitored and sized for demand. |
| Problem and Incident Management | Tell restoring service apart from fixing root causes. |
| IT Change, Configuration, and Patch Management | Assess control over every change to production. |
| Operational Log Management | Check logs are captured, protected, retained and reviewed. |
| IT Service Level Management | Review service levels, how they are measured and reported. |
| Database Management | Assess database integrity, access, backup and administration. |

| Part B: Business Resilience (official topics) | What you need to be able to do |
|---|---|
| Business Impact Analysis | Check critical processes and recovery targets are identified. |
| System and Operational Resilience | Assess redundancy and fault tolerance. |
| Data Backup, Storage, and Restoration | Verify backups exist, are protected and can be restored. |
| Business Continuity Plan | Evaluate the plan, its ownership and its testing. |
| Disaster Recovery Plans | Evaluate IT recovery arrangements and tests. |

## Key concepts

### Asset management and IT components

An accurate inventory, often held in a **configuration management database (CMDB)**, records each asset, its owner, location, configuration and relationships. Without it you cannot patch, license, secure or recover what you have. Software licence compliance and secure disposal at end of life are part of asset management.

### Job scheduling and automation

Production jobs should run from an approved schedule. Changes to schedules and job parameters go through change management. Operators should not be able to alter programs or data outside approved procedures. Job logs and exception reports are reviewed, and failed jobs are handled through a documented process.

### System interfaces

When data moves between systems, the risks are loss, duplication and alteration. Controls include record counts and control totals reconciled between sending and receiving systems, error and exception handling with follow-up, interface monitoring, and secure transfer methods. An unreconciled interface feeding the general ledger is a classic audit finding.

### Shadow IT and end-user computing

**Shadow IT** is technology used without IT's approval or knowledge, such as an unsanctioned cloud service. **End-user computing (EUC)** covers applications users build themselves, especially spreadsheets and small databases. Risks: no change control, errors in formulas, no backup, no access control, and sensitive data in unknown places. Controls: an inventory of critical EUC tools, risk ranking, protected formulas, version control, input checks, independent review of results, and backup. For shadow IT: discover it, assess the data and risk, and bring it under governance.

### Availability and capacity

Monitor performance and utilisation, forecast demand, and plan capacity before it runs out. Availability is usually measured against service levels.

### Incident and problem management

| | Incident management | Problem management |
|---|---|---|
| Goal | Restore normal service as quickly as possible | Find and remove the root cause |
| Trigger | An unplanned interruption or degradation | Recurring or significant incidents |
| Output | Service restored, incident record | Known error, permanent fix, often through a change |

### Change, configuration and patch management

- **Change management:** request, impact assessment, approval, testing, scheduled implementation with a back-out plan, and post-implementation review. Emergency changes follow a faster path but are documented and approved afterwards. Segregation matters: the person who writes a change should not move it to production alone.
- **Configuration management:** keep systems at approved baselines and record the configuration of each item, so unauthorised changes can be detected.
- **Patch management:** track vendor releases, assess and prioritise by risk, test, deploy through change management, verify, and report. A useful measure is the share of critical patches applied within the agreed time.

### Operational log management

Logs should be generated for key events, time-synchronised, protected from alteration and deletion (for example by forwarding them to a central system that system administrators cannot modify), retained for a defined period, and reviewed. A log no one reviews is evidence, not a control.

### Service level management

| Agreement | Between |
|---|---|
| Service level agreement (SLA) | IT or a provider and the business, for a service |
| Operational level agreement (OLA) | Internal IT teams that support the service |
| Underpinning contract | IT and an external supplier that supports the service |

The auditor checks that service levels are defined in measurable terms, monitored with reliable data, reported, and acted on when missed.

### Database management

The database administrator (DBA) manages structure, performance, access and backup, and is a powerful role that needs monitoring. Controls: **referential integrity** (every reference points to an existing record), normalisation to reduce redundant data, concurrency controls to stop conflicting updates, access controls down to tables or fields, logging of DBA activity, and backups with tested restores.

### Business impact analysis

The BIA identifies critical business processes, the impact of their loss over time, the systems and resources they depend on, and their recovery targets. It drives the priorities in the business continuity and disaster recovery plans. It should be updated when the business or its systems change significantly.

| Term | Meaning |
|---|---|
| Recovery time objective (RTO) | How quickly a process or system must be restored |
| Recovery point objective (RPO) | How much data loss, measured in time, is acceptable; drives backup or replication frequency |
| Maximum tolerable downtime | The longest outage before the damage is unacceptable |
| Service delivery objective | The level of service needed during the recovery period |

A short RTO and short RPO cost more. The BIA lets the business choose where that cost is justified.

### Resilience

Redundant components, clustering and failover, load balancing, RAID storage, redundant network links and power, and geographically separated sites all reduce the chance that one failure stops a service. RAID protects against disk failure but is not a backup.

### Backup, storage and restoration

| Backup type | Contents | To restore |
|---|---|---|
| Full | Everything | The last full |
| Incremental | Changes since the last backup of any kind | The last full plus every incremental since |
| Differential | Changes since the last full | The last full plus the latest differential |

- Rotation schemes such as grandfather-father-son keep daily, weekly and monthly copies.
- Store copies offsite or in a separate cloud region, far enough to escape the same disaster, and keep at least one copy offline or immutable to resist ransomware.
- Encrypt backups and control access to them.
- **Test restores regularly.** A successful backup job does not prove recovery is possible.
- For short RPOs, nightly backups are not enough: use replication or continuous data protection.

### Business continuity and disaster recovery

The **business continuity plan** keeps critical business processes running; the **disaster recovery plan** restores IT. Both need an owner, defined roles, contact lists, procedures, regular updates and testing.

| Recovery site | Ready | Cost |
|---|---|---|
| Hot | Hours | High |
| Warm | Days | Medium |
| Cold | Weeks | Low |
| Mirrored or active-active | Near instant | Highest |
| Reciprocal agreement | Uncertain | Low, but rarely enforceable or big enough |

| Plan test | What happens |
|---|---|
| Checklist (desk check) | Plan reviewed by each team for accuracy |
| Structured walkthrough or tabletop | Team talks through a scenario |
| Simulation | Scenario rehearsed realistically, without moving operations |
| Parallel | Recovery site brought up and processing tested while production keeps running |
| Full interruption | Production shut down and moved to recovery; most realistic, most risky |

The auditor checks that the plan is based on a current BIA, tested regularly, updated after tests and changes, and that test results are reviewed by management.

## How the questions look

Expect operational scenarios: an outage, a failed job, a spreadsheet used in financial close, a backup report, a BCP test, a recovery site contract. Questions ask for the GREATEST concern, the BEST evidence, the BEST control, or what the auditor should do FIRST. Many are about recovery: does the arrangement actually meet the business's RTO and RPO?

## A method that works

1. **Find the business requirement.** What does the BIA or SLA require? Most recovery questions are answered by matching the arrangement to the requirement.
2. **Prefer evidence of operation over evidence of design.** A tested restore beats a backup policy.
3. **Look for the root cause.** Recurring incidents point to problem management.
4. **Check that every change went through change management,** including emergency ones and job schedule changes.
5. **For data moving between systems, look for reconciliation.**
6. **Report, do not fix.** As the auditor, you assess and recommend.

## Traps that cost points

- **Treating backup success logs as proof of recovery.** Only restores prove it.
- **Storing backups next to the systems they protect.** One fire destroys both.
- **Confusing incident and problem management.** Restore service versus fix the cause.
- **Accepting a recovery site that cannot meet the RTO.** A cold site for a four-hour RTO is a finding.
- **Overlooking spreadsheets.** A critical EUC tool with no controls is a real risk.
- **Missing the need for a current BIA.** A plan built on an old BIA protects the wrong things.
- **Thinking RAID replaces backups.** It does not protect against deletion, corruption or ransomware.
- **Letting logs be editable by the people they monitor.** Protect them centrally.
- **Accepting an SLA without measurement.** If it is not measured, it is not managed.

## Timing

As guidance, 70 to 90 seconds for scenario items here, and 45 to 60 for recall items such as backup types or site types. With about a quarter of the exam in this domain, it is worth the time to get these tables automatic.

## Practice items

These 4 items are original, written for these notes. They are not taken from ISACA or any prep provider.

### Set 1

**Item 1.** The same database outage has happened on the first business day of each of the last four months. Each time, service was restored by restarting the server. Which process should now address this?

- A. Incident management
- B. Problem management
- C. Capacity management
- D. Service level management

**Item 2.** A trading database has a recovery point objective of 15 minutes. Which arrangement meets it?

- A. A full backup every night, stored offsite
- B. A weekly full backup with daily incremental backups
- C. Near-real-time replication to a secondary site
- D. A monthly backup copied to tape

**Item 3.** Backup jobs report success every night. What is the BEST evidence that data can be recovered?

- A. The backup software's nightly job logs
- B. The backup policy approved by the CIO
- C. The backup vendor's certificate that the software is compatible with the servers
- D. Records of regular test restores of production data

**Item 4.** An IS auditor reviewing change management finds several changes in production with no record of approval. What should the auditor do?

- A. Reverse the changes until they can be approved
- B. Approve the changes retrospectively on management's behalf so that the change records are complete
- C. Ignore them if the systems are working normally
- D. Determine the extent and impact of the unapproved changes and report the finding

<details>
<summary>Answers and explanations, items 1 to 4</summary>

**Item 1: B.** Recurring incidents point to an underlying problem. Problem management investigates the root cause and drives a permanent fix. *Why not A:* incident management has already restored service each time, which is why the outage keeps returning. *Why not C:* capacity might turn out to be the cause, but investigating the cause is problem management's job.

**Item 2: C.** An RPO of 15 minutes allows no more than 15 minutes of data loss, so data must be copied continuously or nearly so. *Why not A:* a nightly backup could lose up to a day of trades. *Why not B:* daily incrementals still allow up to a day of loss.

**Item 3: D.** Only a restore proves that backups are complete and usable. *Why not A:* a success message shows the job ran, not that the data can be restored. *Why not B:* a policy shows intent, not operation.

**Item 4: D.** The auditor assesses how widespread the problem is and its impact, then reports it so management can act. *Why not A:* reversing changes is a management action and could cause outages. *Why not B:* approving changes is management's responsibility, and doing it would impair independence.

</details>

Want more? The [free timed CISA practice test on PrepClubs](https://prepclubs.com/free-practice-tests/cisa?utm_source=github&utm_medium=referral&utm_campaign=study-notes&utm_content=cisa) has 25 questions across all five domains, with your score broken down by domain.

## Score yourself

| Item | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Answer | B | C | D | D |

- **4:** strong. Keep this domain fresh with mixed sets; it is a quarter of the exam.
- **3:** sort misses into operations and resilience, then drill the tables for the weaker half.
- **2 or fewer:** rebuild the backup, site and plan test tables from memory, reread the incident versus problem distinction, then redo the items.

## Next step

With so much weight here, timed practice pays off. Try the [free CISA practice test on PrepClubs](https://prepclubs.com/free-practice-tests/cisa?utm_source=github&utm_medium=referral&utm_campaign=study-notes&utm_content=cisa), then return to the traps list for anything you missed.

## Sources for this page

- [ISACA CISA exam content outline](https://www.isaca.org/credentialing/cisa/cisa-exam-content-outline), for the topics and weight

---

<!-- nav:bottom -->
← Previous: [Domain 3: Acquisition, Development and Implementation](acquisition-development-and-implementation.md) | Next: [Domain 5: Protection of Information Assets](protection-of-information-assets.md) → | [Back to contents](../../README.md#contents)
<!-- /nav:bottom -->
