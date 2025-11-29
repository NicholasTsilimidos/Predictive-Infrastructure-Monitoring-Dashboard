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
## Methodology
Setup and Environment:
To complete this project, we created a controlled testing environment using VirtualBox. Inside VirtualBox, we installed Ubuntu Linux, which served as the server for running Zabbix. This virtual machine acted as the main monitoring system. we also ensured that the VM had internet access so Zabbix could monitor the UAlbany website.

Tools, Frameworks, and Resources:
- VirtualBox: to run the Ubuntu virtual machine
- Ubuntu Linux: operating system for installing Zabbix
- Zabbix Server: main monitoring tool
- Zabbix Frontend – for configuring hosts and viewing dashboard
- Zabbix Agent – installed on the Ubuntu VM to collect host performance data
- Database: MySQL

Resources Monitored:
- UAlbany Website (ualbany.edu): monitored through HTTP checks
- Ubuntu Virtual Machine: monitored through Zabbix Agent.

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

## Conclusion

In this project, Zabbix was successfully installed and configured on an Ubuntu virtual machine to monitor both an external website and a local system. By setting up web monitoring for the UAlbany website and deploying the Zabbix Agent on the Ubuntu host, the project demonstrated how real-time system data, performance metrics, and availability checks can be collected and analyzed through a centralized dashboard. This hands-on experience showed how monitoring tools play a vital role in cybersecurity by helping detect problems early, identify unusual activity, and maintain system reliability.

Future enhancements can include fully implementing email alerting, monitoring multiple hosts, and applying anomaly detection models for predictive risk analysis. Overall, the project provided valuable practical skills in Linux administration, system monitoring, and the use of open-source tools that are essential for cybersecurity and digital forensics work.

---

## Documentation & Report
For full technical details, screenshots, configuration steps, and results:

- **Final Project Report:** Predictive Infrastructure Monitoring Dashboard Using Zabbix (PDF)
- **Installation Guide:** Zabbix Installation & Configuration Guide (PDF)
- **Supporting Documents:** See `/documentation` folder

---

## Potential Improvements

Future enhancements could include expanding monitoring to additional hosts, enabling email alerting, and applying anomaly detection techniques for improved predictive analysis.
