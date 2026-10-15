# KAN-112: DAY 5 |TASK4|Configure Prometheus and Grafana for AWS EC2 Infrastructure Monitoring

- **Jira:** https://sasidharana504.atlassian.net/browse/KAN-112
- **Status:** Review
- **Assignee:** sasidharana504
- **Issue type:** Task
- **Priority:** Medium
- **Resolution:** —
- **Reporter:** sasidharana504
- **Created:** 2026-10-15T12:15:13.908Z
- **Updated:** 2026-10-15T12:16:26.525Z
- **Due date:** —
- **Labels:** —
- **Components:** —

## Description

Description

Set up an infrastructure monitoring solution using Prometheus and Grafana on AWS EC2 instances. Configure Prometheus to collect Linux system metrics from monitored instances using Node Exporter and visualize the collected metrics through Grafana dashboards.

Scope of Work

1. Create three Ubuntu EC2 instances: one dedicated monitoring server and two monitored instances.
2. Install and configure Prometheus on the monitoring server.
3. Configure the Prometheus YAML configuration file with scrape intervals and target endpoints.
4. Install and configure Node Exporter on both monitored EC2 instances.
5. Configure AWS Security Groups to allow required monitoring traffic securely.
6. Verify that Prometheus collects metrics successfully from all configured targets.
7. Install Grafana and configure Prometheus as its data source.
8. Import and configure a suitable Grafana dashboard to visualize CPU, memory, disk, and network metrics.
9. Validate the monitoring setup and document the configuration and results.
Technical Requirements

- Prometheus: Port 9090
- Grafana: Port 3000
- Node Exporter: Port 9100
- Scrape interval: 15 seconds
- Operating system: Ubuntu Linux
- Infrastructure: AWS EC2
Acceptance Criteria

- Prometheus is installed and running successfully.
- Node Exporter is running on both monitored EC2 instances.
- Prometheus configuration includes all required scrape targets.
- All configured targets show UP on the Prometheus Targets page.
- Grafana is successfully connected to Prometheus.
- A Grafana dashboard displays infrastructure metrics, including CPU, memory, disk, and network usage.
- Security Groups restrict access to monitoring ports to authorized sources.
- Screenshots of Prometheus targets and the Grafana dashboard are attached.
- Installation steps, configuration details, and validation results are documented.
Deliverables

- Working Prometheus monitoring server.
- Two monitored EC2 instances configured with Node Exporter.
- Grafana dashboard connected to Prometheus.
- Configuration files and validation screenshots.
- Brief documentation of the setup and troubleshooting performed.
Notes

Use private IP addresses for communication between EC2 instances wherever possible. Restrict web interface access to authorized IP addresses and Node Exporter access to the monitoring server. Review potential AWS infrastructure charges before creating resources and terminate lab instances when they are no longer required.

Priority: Medium

Labels: AWS, Prometheus, Grafana, Monitoring, DevOps

## Attachments

- [Screenshot 2026-10-15 at 5.41.16 PM.png](attachments/Screenshot%202026-10-15%20at%205.41.16%20PM.png)
- [Screenshot 2026-10-15 at 5.41.27 PM.png](attachments/Screenshot%202026-10-15%20at%205.41.27%20PM.png)
- [Screenshot 2026-10-15 at 5.42.03 PM.png](attachments/Screenshot%202026-10-15%20at%205.42.03%20PM.png)
- [Screenshot 2026-10-15 at 5.42.30 PM.png](attachments/Screenshot%202026-10-15%20at%205.42.30%20PM.png)
- [Screenshot 2026-10-15 at 5.42.44 PM.png](attachments/Screenshot%202026-10-15%20at%205.42.44%20PM.png)
- [Screenshot 2026-10-15 at 5.42.51 PM.png](attachments/Screenshot%202026-10-15%20at%205.42.51%20PM.png)
