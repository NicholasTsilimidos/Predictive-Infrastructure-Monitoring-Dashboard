Final project for BFOR419/519 — Predictive Infrastructure Monitoring Dashboard Using Zabbix.

Group Members - Saimanikanta Reddy, Rachael Oyenola, Nicholas Tsilimidos

**Project Overview: A brief summary of your project, what it does, and the main objective.

Our project focuses on building a Predictive Infrastructure Monitoring Dashboard using Zabbix, an open-source monitoring platform widely used in cybersecurity, system administration, and incident response. The goal of the project is to demonstrate how early detection of performance issues such as rising CPU usage, memory saturation, disk exhaustion, or website downtime can significantly reduce system failures and improve overall reliability.

Our setup uses a Zabbix Server running on Linux inside a VirtualBox, along with monitored hosts and website checks. Through different Zabbix Agents and Web Scenarios, the system continuously collects performance metrics, visualizes them in real time, and triggers alerts whenever abnormal activity is detected on the University at Albany website. By leveraging Zabbix’s built-in trend analysis, the project highlights how predictive monitoring can help administrators identify problems before they lead to outages or any cyber-related attacks.

The main objective of this project is to build a fully functional monitoring environment accompanied by a structured dashboard, alert configurations, and data-flow documentation. This demonstrates how Zabbix can be used as a proactive monitoring solution to support uptime, operational stability, and infrastructure resilience in real-world environments.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**Project Relevance: Explain why this problem or tool matters in cybersecurity/forensics. Why did you choose it? What skills or knowledge can someone gain from this work?

Predictive monitoring plays a critical role in cybersecurity and digital forensics because many incidents begin with subtle anomalies long before a system fully fails. Tools like Zabbix allow people to detect early warning signs such as unexplained CPU spikes, memory exhaustion, slow website response times, unauthorized downtime, or abnormal network traffic that may indicate emerging vulnerabilities. By continuously collecting and storing system data, Zabbix supports real-time visibility as well as forensic reconstruction after an incident occurs.

We chose Zabbix for this project because it is a widely used, open-source monitoring solution that mirrors what real organizations use in system administration and cybersecurity environments. It provides hands-on exposure to concepts that cybersecurity professionals rely on daily, such as alerts, trend analysis, host monitoring, and understanding system health indicators. Monitoring the University at Albany website, along with the Linux host on a Virtual Machine allowed us to simulate real-world scenarios where early detection directly prevents downtime and reduces the impact of cyber-related attacks.

This project helps develop practical skills that are valuable in cybersecurity and digital forensics, including configuring monitoring agents, interpreting system metrics, detecting anomalies, and understanding service availability. These skills are essential for SOC analysts, incident responders, and forensic investigators who rely on accurate system data to identify threats, troubleshooting issues, and prevent outages. Overall, the project demonstrates how proactive monitoring strengthens system reliability, enhances visibility, and contributes to a stronger defensive posture in modern IT environments.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**Project Architecture & Workflow

The architecture of our predictive monitoring environment is built around a Zabbix Server running on a Linux Virtual Machine, supported by a monitored Linux host and a web scenario designed to track the performance of the University at Albany website. This setup mirrors real-world monitoring infrastructures used in cybersecurity, IT operations, and system administration.

System Architecture:

1. Zabbix Server (Linux VM)
•	Hosts the Zabbix frontend, server process, and MySQL database
•	Receives data from monitored hosts
•	Processes alert logic, triggers, and trend analysis
•	Displays metrics and dashboards through the web interface

2. Monitored Linux Host (Second VM)
•	Runs the Zabbix Agent to collect local system metrics
•	Sends CPU, memory, disk, and network data to the Zabbix Server
•	Appears as a monitored host with individual dashboards and graphs

3. Website Monitoring (UAlbany Web Scenario)
•	Uses Zabbix’s Web Scenario feature
•	Performs HTTP checks on the UAlbany website
•	Verifies availability, response time, and response codes
•	Triggers alerts when the website becomes slow or unreachable

4. MySQL Database (within Zabbix Server VM)
•	Stores history data (high-resolution metrics)
•	Stores trend data (hourly aggregates for prediction)
•	Supports analysis and long-term monitoring

5. VirtualBox Environment
•	Provides isolated VMs for the Zabbix server and monitored hosts
•	Ensures a controlled environment for testing and data collection
•	Reflects common lab setups used in cybersecurity programs

Workflow Overview:

1. Data Collection
•	Zabbix Agent on the Linux host sends system metrics to the server
•	Web Scenario performs recurring checks on the UAlbany website
•	Zabbix Server records raw metrics and stores them in MySQL

2. Processing & Evaluation
•	Zabbix applies built-in thresholds and custom triggers
•	Metrics are evaluated in real time for anomalies
•	Trend data is aggregated for long-term analysis

3. Alerting
•	If performance drops below expected thresholds
•	Zabbix generates alerts
•	Email alerts and trigger logic are configured to notify administrators

4. Visualization (Zabbix dashboards display)
•	CPU/memory/disk graphs
•	Network traffic charts
•	Website response time and availability
•	Trigger status and historical trends

5. Predictive Monitoring
•	Zabbix identifies long-term patterns (disk growth, CPU trends)
•	Trend data allows administrators to anticipate potential failures
•	Supports proactive response rather than reactive troubleshooting

Architecture Summary:
This workflow demonstrates how a real monitoring environment operates in cybersecurity and IT operations. Our architecture shows how monitored data flows from a host and website into the Zabbix Server, then into the database, and finally into dashboards, alerts, and trend analysis tools. This setup allows organizations to detect problems early, maintain availability, and strengthen their operational resilience.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

5. Methodology (How We Built It)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
   
**Data Used

Zabbix collects real-time system and service data from both monitored hosts and web targets. For this project, the monitored data includes:

Linux Host Metrics (Zabbix Agent)
•	CPU Usage: Processor load over time to detect spikes or abnormal usage.
•	Memory Utilization: Tracks available vs. used RAM to identify saturation.
•	Disk Usage: Storage consumption, remaining free space, and early signs of exhaustion.
•	Network Traffic: Inbound and outbound packet rates and unusual communication spikes.
•	System Uptime: Verifies host stability and unexpected reboots.

Website Monitoring (Web Scenario)
•	HTTP Response Codes: Ensures the University at Albany website is returning 200 OK.
•	Website Reachability: Alerts if the site becomes inaccessible.
•	Response Time: Measures how long the site takes to load.
•	Step Validation: Verifies multiple checks within the scenario for consistency.

Zabbix Internal Data:
Zabbix also records server performance metrics such as different processes, queue sizes, and agent availability, which help validate the health of the monitoring environment.
Historical & Trend Data:

Zabbix stores two types of data in its database:
•	History Data: High-resolution metrics used for short-term monitoring.
•	Trend Data: Aggregated hourly and daily values used for long-term analysis and forecasting.

This data forms the foundation of the dashboard visualizations, alert triggers, and predictive monitoring used in our project.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

7. Results (Screenshots, Alerts, Trends)

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**Conclusion & Next Steps

This project demonstrated how Zabbix can be used as an effective tool for proactive and predictive infrastructure monitoring. By setting up a Zabbix Server, configuring a monitored Linux host, and creating a web scenario from the University at Albany website, we were able to show how early detection of performance issues can prevent outages and reduce the impact of system failures. Zabbix’s ability to collect continuous metrics, visualize system behavior in real time, and generate alerts when thresholds are exceeded highlights its value in both cybersecurity and system administration environments.

Working with Zabbix also provided hands-on experience with critical skills used by SOC analysts, incident responders, and system administrators. These include configuring monitoring agents, interpreting system metrics, detecting anomalies, and understanding how systems support both operational monitoring and forensic analysis. Through this project, we gained a deeper understanding of how predictive monitoring improves system reliability, enhances visibility, and strengthens the overall defensive posture of an organization.

Overall, this project reinforced the importance of monitoring tools in modern IT environments and demonstrated how platforms like Zabbix can support uptime, improve response times, and offer insights that help prevent issues before they escalate as well. As organizations continue to rely on complex infrastructures, tools like Zabbix play a key role in ensuring stability, security, and operational resilience.

Future improvements could also include integrating and testing the full email alerting system, expanding monitoring to additional hosts or services, and applying Zabbix’s forecasting capabilities to provide a more secure trend analysis. These enhancements would strengthen the predictive monitoring environment even further and provide deeper insight into system performance and potential failures.
