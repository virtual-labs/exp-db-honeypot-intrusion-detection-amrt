
### Database Honeypot: Theory and Concept

A **honeypot** is a security mechanism designed to detect, deflect, and analyze unauthorized access attempts by intentionally deploying a controlled and monitored decoy system that appears to contain valuable resources.

In the context of **database security**, a **honeypot database** is created as a decoy environment that mimics a legitimate database system and contains fabricated sensitive data such as:

- User credentials
- Financial records
- Confidential information

#### Fundamental Principle

The core idea behind a honeypot is **deception-based defense**.

While traditional security mechanisms focus on **prevention**:

- Authentication
- Encryption
- Firewalls
- Access controls

a honeypot operates under the assumption that an attacker **may bypass** these preventive controls. Therefore, a decoy database is introduced to act as a trap.

Main objectives:

- Early detection of malicious activities
- Observation of attacker behavior
- Collection of intelligence about attack techniques

#### Implementation in This Experiment

Fake sensitive tables are created, for example:

- `users_decoy`
- `credit_cards_decoy`
- `banking_records_decoy`
- `employee_payroll_decoy`

These tables are **not accessed** during normal system operations.

**Any interaction** with these tables — including:

- `SELECT`
- `INSERT`
- `UPDATE`
- `DELETE`
- `DROP`
- `ALTER`

is considered **suspicious** and is recorded.

#### What the System Monitors

In this experiment, you can monitor the attacker's activity using:

- **Query Logging**: Records all SQL activity within the honeypot database.
- **Intrusion Alerts**: Sends immediate notifications upon detection of suspicious behavior.
- **Real-time Monitoring**: Actively detects and flags attacker interactions as they happen.

#### Alerting and Logging

When an unauthorized user interacts with the honeypot database, the system:

1. Generates **real-time alerts**
2. Stores detailed logs containing:

   - **Timestamp**: Time of access
   - **Action**: Type of activity (e.g., Login Success, Data Access, Dump Attempt)
   - **Status**: Whether the action is considered Normal or Suspicious
   - **Details**: Specific information such as the source IP or exact query executed

#### Benefits and Purpose

The collected information is analyzed to:

- Understand current attacker techniques and TTPs (Tactics, Techniques, and Procedures)
- Identify previously unknown vulnerabilities or misconfigurations
- Improve database security policies
- Enhance rules for intrusion detection systems (IDS/IPS)
- Support forensic investigations
- Provide early warning of potential breaches

#### Important Characteristics

- The honeypot database is **not** a production system
- It **does not** store real sensitive data
- It **complements** (does not replace) traditional security controls
- Acts as an **additional layer** of defense through controlled deception and activity logging

In summary, in this experiment the honeypot database functions primarily as a **detection and monitoring tool** rather than a preventive barrier.
