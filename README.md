# Predictive Infrastructure Monitoring Dashboard Using Zabbix

**Course:** BFOR419/519 – System Administration & Operating Systems Concepts  
**Team Members:** Reddy Sai Manikanta, Rachael Oyenola, Nicholas Tsilimidos  

---

## Project Overview
This project implements a predictive infrastructure monitoring system using Zabbix to detect early signs of system failures and service disruptions. The monitoring environment uses a Linux-based Zabbix Server hosted in a virtual machine to collect and analyze performance metrics from a monitored Linux host and an external website.

The goal of the project is to demonstrate how predictive monitoring can reduce downtime by identifying performance issues such as CPU spikes, memory exhaustion, disk saturation, and website availability problems before they lead to system failure.

---

## Why This Matters (Relevance)
Predictive monitoring is an important capability in cybersecurity because many security incidents and system failures begin as subtle performance anomalies. Tools like Zabbix help detect early warning signs that may indicate misconfigurations, failures, or suspicious behavior.

This project connects directly to:
- Incident response and forensic investigation
- Security operations monitoring (SOC)
- Infrastructure hardening and uptime assurance
- Defensive cybersecurity operations

---

## System Architecture
The environment consists of:
- One Linux Virtual Machine running the Zabbix Server, database, and frontend
- One Linux host monitored using the Zabbix Agent
- A monitored web target (UAlbany website) using Zabbix web scenarios

Data flows from the Zabbix Agent to the Zabbix Server, into the database, and is visualized on the dashboard where alerts and triggers are evaluated.

---

## Data Used
The monitoring platform collected the following data:
- CPU utilization
- Memory usage
- Disk usage
- Network traffic
- System uptime
- HTTP response codes and website availability
- Historical and trend metrics for analysis

---

## Results Summary
The system successfully monitored a Linux host and external website using real-time metrics and triggers. The dashboard visualized performance behavior, and alerts were generated when thresholds were exceeded.

These results demonstrate how predictive monitoring improves visibility and incident readiness in cybersecurity environments.

---

## Documentation & Report
For full technical details, screenshots, configuration steps, and results:

- **Final Project Report:** Predictive Infrastructure Monitoring Dashboard Using Zabbix (PDF)
- **Installation Guide:** Zabbix Installation & Configuration Guide (PDF)
- **Supporting Documents:** See `/documentation` folder

---

## Potential Improvements

Future enhancements could include expanding monitoring to additional hosts, enabling email alerting, and applying anomaly detection techniques for improved predictive analysis.
