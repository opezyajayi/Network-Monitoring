📊 Splunk – Monitoring, Security & Log Analysis
🔍 Overview

Splunk is a powerful data analytics platform used to collect, search, analyze, and visualize machine-generated data such as logs, metrics, and events. It is widely adopted for SIEM, security monitoring, IT operations, and troubleshooting.

This repository documents core Splunk concepts, SPL queries, dashboards, and practical use cases focused on cybersecurity and operational visibility.

🚀 Key Features

Real-time log ingestion and analysis

Search Processing Language (SPL) for advanced querying

Interactive dashboards and visualizations

Alerting and automation

Security Information and Event Management (SIEM) capabilities

🧠 Core Concepts Covered

Indexes, sourcetypes, and events

SPL fundamentals

Dashboards and panels

Alerts and reports

Roles and access control

Splunk architecture (Forwarder, Indexer, Search Head)

🔐 Security Use Cases

Failed login detection

Brute-force attack monitoring

Malware and IDS alert analysis

User behavior analytics

Compliance and audit logging

MITRE ATT&CK–aligned detections

🖥️ IT Operations Use Cases

Server performance monitoring

Application error tracking

Resource utilization (CPU, memory, disk)

System availability and uptime

📊 Dashboards

Splunk dashboards transform raw logs into actionable insights.

Examples included:

SOC overview dashboard

Authentication monitoring

System health dashboard

Top alerts and incidents

🧪 Sample SPL Queries
Failed Login Attempts
index=security sourcetype=authentication action=failure
| stats count by user, src_ip
| sort -count

Top Error Messages
index=app_logs level=error
| stats count by message
| sort -count

System Resource Usage
index=os sourcetype=cpu
| timechart avg(cpu_usage) by host

🛠️ Tools & Integrations

Splunk Enterprise / Splunk Cloud

Universal Forwarder

Syslog sources

Firewalls, IDS/IPS

Endpoint and authentication logs

📁 Repository Structure
splunk/
├── dashboards/
│   ├── soc_dashboard.json
│   ├── system_health.xml
├── spl_queries/
│   ├── security_queries.spl
│   ├── ops_queries.spl
├── docs/
│   ├── splunk_basics.md
│   ├── dashboard_design.md
└── README.md

🎯 Learning Objectives

Understand how Splunk ingests and processes data

Write effective SPL queries

Build meaningful dashboards

Apply Splunk in real-world cybersecurity scenarios

📚 References

Splunk Documentation

Splunk Security Essentials

MITRE ATT&CK Framework

👤 Author

Ope Ajayi
Cybersecurity | SIEM | Threat Detection
