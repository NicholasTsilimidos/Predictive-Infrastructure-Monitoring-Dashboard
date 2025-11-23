This directory contains configuration files used during the Zabbix setup and monitoring process.

Potential files that can be added:
- zabbix_server.conf — Main Zabbix server configuration file (with database and service parameters).
- zabbix_agentd.conf — Configuration file used for monitored clients (agents) to send metrics to the server.
- alertscript configurations (if applicable)
- email notification configuration (SMTP settings if exported)
- Virtual machine environment notes (network settings, hostnames, IP assignments)

These files are included for transparency and reproducibility, allowing others to recreate the same monitoring environment.
