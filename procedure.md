#### Step 1: Introduction to Database Honeypots

- Read the introduction to understand the core concept of a database honeypot.
- Review the **Bank Vault Analogy** to understand how a decoy database protects the real production environment.
- Click **Start Lab** to begin the simulation.

  <img src="images/intro.png" alt="Honeypot Introduction" width="800">

#### Step 2: Create Fake Sensitive Tables

- Select one or more **decoy data tables** (e.g., **Users**, **Credit Cards**, **Banking Records**) to serve as simulated sensitive data.
  
  <img src="images/deploy_decoy_1.png" alt="Selecting Decoy Data Tables" width="800">

- Note that deploying multiple decoy tables makes the honeypot appear more realistic to potential attackers.
- Click **Deploy Honeypot** to initialize the decoy database.
  
  <img src="images/deploy_decoy_2.png" alt="Deployed Decoy Database" width="800">

- Click **Next: Monitoring** to proceed.

#### Step 3: Configure Security Monitoring

- Choose the security monitoring tools required to monitor the honeypot:
  - **Query Logging:** Records all executed SQL queries for analysis.
  - **Intrusion Alerts:** Sends immediate notifications upon detecting suspicious activity.
  - **Real-time Monitoring:** Actively flags attacker interactions as they occur.
- Enable the desired options to maximize system protection and monitoring coverage.
  
  <img src="images/configure_monitoring_1.png" alt="Configuring Security Monitoring Tools" width="800">

- Click **Start Monitoring** to activate the selected security measures.
- Once a security alert is triggered, click **Proceed to Security Analysis**.

  <img src="images/configure_monitoring_2.png" alt="Monitoring Active State" width="800">

#### Step 4: Monitor Attack Interactions

- Observe the **Live Attack Console** as it simulates a real-time external intrusion.
- Monitor the execution of unauthorized queries (e.g., `SHOW TABLES;`, `SELECT`) targeting the decoy database.

  <img src="images/simulated_attack_1.png" alt="Observing Simulated Attack Console" width="800">

- Wait for the system to detect the intrusion and trigger a **Security Alert**, then click **View Alert**.

  <img src="images/simulated_attack_2.png" alt="Security Alert Triggered" width="800">

- Review the incident summary details, then click **Proceed to Incident Analysis**.

  <img src="images/simulated_attack_3.png" alt="Incident Summary Alert" width="800">

#### Step 5: Analyze Attacker Behaviour (Log Analysis)

- Assume the role of a Security Consultant and investigate the attack activity logs.
- Review the attack timeline to understand the sequence from initial discovery to data theft.
- Analyze the log entries generated in the **Highlighted Logs Panel**.
- Identify and select the specific log entries that indicate suspicious data access or database dumping.

  <img src="images/log_analysis_1.png" alt="Log Analysis Selection" width="800">

- Monitor the **Suspicion Meter** as validation for selecting the correct malicious logs.
- Click **Submit Analysis** to verify your investigation. You can click **Restart** to retry the simulation with different configurations.

  <img src="images/log_analysis_2.png" alt="Security Analysis Completed" width="800">