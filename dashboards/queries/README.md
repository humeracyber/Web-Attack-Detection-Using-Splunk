🔐 Web Attack Detection Dashboard (Splunk SIEM Project)

📌 Overview

This project is a Security Information and Event Management (SIEM) use case built using Splunk.
It analyzes HTTP logs to detect common web attacks such as brute force login attempts, SQL injection, suspicious file access, and command execution attempts.

The goal is to simulate real-world SOC (Security Operations Center) monitoring.

⸻

🎯 Objectives

* Detect brute force login attempts
* Identify SQL injection attacks
* Monitor sensitive file access
* Detect suspicious file uploads
* Track web shell / command execution activity
* Visualize attack patterns using Splunk dashboards

⸻

🧰 Tools Used

* Splunk Enterprise / Splunk Cloud
* Custom HTTP log dataset (http_custom_logs)
* SPL (Search Processing Language)

⸻

🚨 Threat Detection Use Cases

1. Brute Force Attacks

Detects repeated failed login attempts using HTTP status 401.

2. Successful Logins

Tracks successful authentication attempts using HTTP status 200.

3. SQL Injection Attempts

Detects malicious patterns like:

* OR
* UNION
* SELECT
* Special characters like ' and ;

4. Sensitive File Access

Monitors access to sensitive files such as:

* .zip
* .db

5. Suspicious File Uploads

Detects uploads through endpoints like upload.php.

6. Web Shell / Command Execution

Identifies command injection attempts using parameters like cmd=.

⸻

📊 Dashboard Features

* Total HTTP traffic overview
* Brute force attack tracking by source IP
* Successful login monitoring
* SQL injection detection panel
* Suspicious file access tracking
* Attack timeline visualization

📁 Project Structure

web-attack-detection-splunk/
│
├── dashboards/
│   └── http_attack_dashboard.xml
│
├── queries/
│   └── spl_queries.txt
│
├── screenshots/
│   ├── dashboard.png
│
└── README.md

📈 SPL Queries

All detection queries used in this project are available in:

queries/spl_queries.txt

🎓 Learning Outcomes

* Understanding web attack patterns
* Writing SPL queries for security detection
* Building SOC-style dashboards in Splunk
* Log analysis and threat hunting basics

⸻

👩‍💻 Author

Humera
Cybersecurity / SOC Analyst Aspirant

⸻

🚀 Future Improvements

* Add alerting for brute force thresholds
* Implement risk scoring for IP addresses
* Add geo-location tracking for attacks
* Integrate with email/SIEM alerts
