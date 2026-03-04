

A **honeypot** is a security mechanism designed to detect, deflect, and analyze unauthorized access attempts by intentionally deploying a controlled and monitored decoy system that appears to contain valuable resources.

In the context of **database security**, a **honeypot database** is created as a decoy environment that mimics a legitimate database system and contains fabricated sensitive data such as:

- User credentials
- Financial records
- Confidential information

#### Fundamental Principle

The core idea behind a honeypot is **deception-based defense**.

While traditional security mechanisms focus on **prevention**, such as:

- Authentication
- Encryption
- Firewalls
- Access controls

a honeypot operates under the assumption that an attacker **may bypass** these preventive controls. Therefore, a decoy database is introduced to act as a trap.

The main objectives of a honeypot system include:

- Early detection of malicious activities
- Observation of attacker behavior
- Collection of intelligence about attack techniques

#### Implementation in This Experiment

In the honeypot database, fake sensitive tables are created such as:

- `users_decoy`
- `credit_cards_decoy`
- `banking_records_decoy`
- `employee_payroll_decoy`

These tables are intentionally isolated and are **not accessed during normal system operations**.

**Any interaction with these decoy tables** — including:

- `SELECT`
- `INSERT`
- `UPDATE`
- `DELETE`
- `DROP`
- `ALTER`

is considered **suspicious** and is recorded for further analysis.

#### What the System Monitors

In this experiment, **attacker activity can be monitored** using the following mechanisms:

- **Query Logging**  
  Records all SQL activity performed within the honeypot database.

- **Intrusion Alerts**  
  Sends immediate notifications when suspicious behavior is detected.

- **Real-time Monitoring**  
  Continuously observes database activity and flags attacker interactions as they occur.

#### Alerting and Logging

When an unauthorized user interacts with the honeypot database, the system performs the following actions:

1. Generates **real-time alerts**
2. Stores detailed logs containing:

   - **Timestamp** – Time of access  
   - **Action** – Type of activity (e.g., Login Success, Data Access, Dump Attempt)  
   - **Status** – Whether the action is considered Normal or Suspicious  
   - **Details** – Additional information such as the source IP address or the exact query executed

#### Benefits and Purpose

The collected information is analyzed to:

- Understand current attacker techniques and **TTPs (Tactics, Techniques, and Procedures)**
- Identify previously unknown vulnerabilities or misconfigurations
- Improve database security policies
- Enhance rules for **Intrusion Detection Systems (IDS)** and **Intrusion Prevention Systems (IPS)**
- Support **digital forensic investigations**
- Provide early warning of potential security breaches

#### Important Characteristics

- The honeypot database is **not a production system**
- It **does not store real sensitive data**
- It **complements (but does not replace)** traditional security mechanisms
- It acts as an **additional layer of defense** through controlled deception and activity monitoring

In summary, the honeypot database in this experiment functions primarily as a **detection and monitoring mechanism rather than a preventive control**. By capturing and analyzing unauthorized interactions with decoy database tables, the system helps security administrators understand attacker behavior and strengthen the overall security posture of the database environment.