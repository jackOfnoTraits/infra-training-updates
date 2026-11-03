# EY403-11: Day 15 - Task 3 - AWS VPC Configuration – Public & Private Subnet Architecture

- **Jira:** https://sasidharana504.atlassian.net/browse/EY403-11
- **Status:** Done
- **Assignee:** sasidharana504
- **Issue type:** Task
- **Priority:** Medium
- **Resolution:** Done
- **Reporter:** sasidharana504
- **Created:** 2026-11-02T09:55:27.852Z
- **Updated:** 2026-11-03T02:23:53.288Z
- **Due date:** —
- **Labels:** —
- **Components:** —

## Description

Design and implement a basic AWS Virtual Private Cloud (VPC) using CIDR 10.0.0.0/16, consisting of exactly two subnets: Public and Private.

Configure network connectivity, routing, security groups, and EC2 instances to understand how public-facing services communicate with privately hosted resources while maintaining network isolation.

Implementation Tasks

1. Create VPC  - Create VPC with CIDR 10.0.0.0/16.
2. Create Subnets  - Public Subnet: 10.0.10.0/24 - Private Subnet: 10.0.20.0/24 - Assign Availability Zones.
3. Configure Internet Gateway (IGW)  - Create and attach an IGW to the VPC.
4. Configure Route Tables  - Public Route Table: Associate with Public Subnet and add 0.0.0.0/0 route through IGW. - Private Route Table: Associate with Private Subnet and configure outbound internet access through NAT Gateway.
5. Configure NAT Gateway  - Deploy a zonal NAT Gateway in the Public Subnet. - Allocate and associate an Elastic IP.
6. Configure Security Groups  - Allow controlled access to private resources from the Public Subnet. - Restrict unnecessary inbound traffic to private resources.
7. Deploy EC2 Instances  - Launch one EC2 instance in each subnet. - Associate appropriate Security Groups. - Configure public/private IP addressing and connectivity.
Expected Outcome

- A functioning VPC with exactly two subnets.
- Public resources accessible through the Internet Gateway, subject to security rules.
- Private resources isolated from direct internet access.
- Private instances able to initiate outbound internet connections through NAT Gateway.
- Controlled communication between public and private EC2 instances.
Deliverables

- VPC and subnet configuration.
- IGW and NAT Gateway configuration.
- Route tables and subnet associations.
- Security Group configurations.
- EC2 connectivity and network isolation verification.
- Architecture diagram documenting the final setup.

## Attachments

- [Screenshot 2026-11-02 at 4.48.37 PM.png](attachments/Screenshot%202026-11-02%20at%204.48.37%20PM.png)
- [Screenshot 2026-11-02 at 4.53.08 PM.png](attachments/Screenshot%202026-11-02%20at%204.53.08%20PM.png)
- [Screenshot 2026-11-02 at 4.55.45 PM.png](attachments/Screenshot%202026-11-02%20at%204.55.45%20PM.png)
- [Screenshot 2026-11-02 at 4.56.33 PM.png](attachments/Screenshot%202026-11-02%20at%204.56.33%20PM.png)
- [Screenshot 2026-11-02 at 4.58.46 PM.png](attachments/Screenshot%202026-11-02%20at%204.58.46%20PM.png)
- [Screenshot 2026-11-02 at 4.58.59 PM.png](attachments/Screenshot%202026-11-02%20at%204.58.59%20PM.png)
- [Screenshot 2026-11-02 at 5.20.29 PM.png](attachments/Screenshot%202026-11-02%20at%205.20.29%20PM.png)
- [Screenshot 2026-11-02 at 5.20.46 PM.png](attachments/Screenshot%202026-11-02%20at%205.20.46%20PM.png)
- [Screenshot 2026-11-02 at 5.20.57 PM.png](attachments/Screenshot%202026-11-02%20at%205.20.57%20PM.png)
- [Screenshot 2026-11-02 at 5.24.33 PM.png](attachments/Screenshot%202026-11-02%20at%205.24.33%20PM.png)
- [Screenshot 2026-11-02 at 5.24.47 PM.png](attachments/Screenshot%202026-11-02%20at%205.24.47%20PM.png)
- [Screenshot 2026-11-02 at 5.42.49 PM.png](attachments/Screenshot%202026-11-02%20at%205.42.49%20PM.png)
- [Screenshot 2026-11-02 at 5.43.23 PM.png](attachments/Screenshot%202026-11-02%20at%205.43.23%20PM.png)
- [Screenshot 2026-11-02 at 5.43.39 PM.png](attachments/Screenshot%202026-11-02%20at%205.43.39%20PM.png)
- [Screenshot 2026-11-02 at 5.43.54 PM.png](attachments/Screenshot%202026-11-02%20at%205.43.54%20PM.png)
- [Screenshot 2026-11-02 at 5.44.04 PM.png](attachments/Screenshot%202026-11-02%20at%205.44.04%20PM.png)
