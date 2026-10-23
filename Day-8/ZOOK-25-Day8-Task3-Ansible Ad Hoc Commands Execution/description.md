# ZOOK-25: Day8-Task3:Ansible Ad Hoc Commands Execution

- **Jira:** https://gomathiboyalla4-1792569022463.atlassian.net/browse/ZOOK-25
- **Status:** Done
- **Assignee:** sasidharana504
- **Issue type:** Task
- **Priority:** Medium
- **Resolution:** Done
- **Reporter:** Sujitha M
- **Created:** 2026-10-22T08:41:05.263Z
- **Updated:** 2026-10-23T06:39:53.504Z
- **Due date:** —
- **Labels:** —
- **Components:** —

## Description

Step 1: Create EC2 Instances
Create four Amazon EC2 Linux instances: one master node and three managed (slave) nodes. Configure the required key pair, security group, and network settings.

Step 2: Install Python and Ansible Using User Data
During instance creation, navigate to Advanced details → User data and provide the installation script.

For the master node:


```
#!/bin/bash
yum install python3-pip -y
pip3 install ansible
```

For each managed node:


```
#!/bin/bash
yum install python3-pip -y
```

Launch all four instances and allow the installation scripts to execute during the initial boot.

Step 3: Configure PuTTY and Pageant
Load the SSH private key into Pageant, configure PuTTY authentication settings, enable agent forwarding if required, and connect to the master node.

Step 4: Verify Python and Ansible Installation
Execute the following commands on the master node:


```
python3 --version
pip3 --version
ansible --version
```

Verify Python availability on the managed nodes:


```
python3 --version
```

Step 5: Create the Ansible Inventory File
Create an inventory file on the master node to store the private IP addresses of the three managed nodes.


```
vi slaves.txt
```

Add the following configuration, replacing the example IP addresses:


```
[slaves]
10.0.1.11
10.0.1.12
10.0.1.13
```

Save and exit the file.

Step 6: Verify SSH Connectivity
Ensure that the master node can connect to all managed nodes using SSH and the appropriate private key and remote username.

Step 7: Test Ansible Connectivity
Execute the following ad hoc command to check connectivity with all managed nodes:


```
ansible all -i slaves.txt -m ping -u ec2-user
```

Verify that all three nodes return successful responses.

Step 8: Retrieve Hostnames
Execute an ad hoc command to retrieve hostnames from the managed nodes:


```
ansible all -i slaves.txt -m command -a "hostname -a" -u ec2-user
```

Step 9: Check System Uptime
Retrieve the system uptime of all managed nodes:


```
ansible all -i slaves.txt -m command -a "uptime" -u ec2-user
```

Step 10: Check Disk and Memory Usage
Execute commands to inspect resource utilization:


```
ansible all -i slaves.txt -m command -a "df -h" -u ec2-user
ansible all -i slaves.txt -m command -a "free -h" -u ec2-user
```

Step 11: Create a Sample HTML File
Create a sample HTML file on the master node:


```
echo "<h1>Ansible Test</h1>" > sample.html
```

Step 12: Copy the File to Managed Nodes
Use the Ansible copy module to transfer the file to all managed nodes:


```
ansible all -i slaves.txt -m copy -a "src=sample.html dest=/tmp/sample.html" -u ec2-user
```

Step 13: Verify File Transfer
Connect to a managed node using SSH and verify the copied file:


```
ssh ec2-user@10.0.1.11
ls -l /tmp/sample.html
cat /tmp/sample.html
```

Repeat the verification on other managed nodes as required.

Expected Outcome:
Successfully create and configure one Ansible master node and three managed nodes, automate Python and Ansible installation using EC2 user data, establish SSH connectivity, execute Ansible ad hoc commands, retrieve system information, and transfer files across the managed infrastructure.

## Attachments

- [Screenshot 2026-10-22 at 9.49.58 PM.png](attachments/Screenshot%202026-10-22%20at%209.49.58%20PM.png)
- [Screenshot 2026-10-22 at 9.50.14 PM.png](attachments/Screenshot%202026-10-22%20at%209.50.14%20PM.png)
- [Screenshot 2026-10-22 at 9.50.28 PM.png](attachments/Screenshot%202026-10-22%20at%209.50.28%20PM.png)
- [Screenshot 2026-10-22 at 9.50.49 PM.png](attachments/Screenshot%202026-10-22%20at%209.50.49%20PM.png)
- [Screenshot 2026-10-23 at 12.07.43 PM.png](attachments/Screenshot%202026-10-23%20at%2012.07.43%20PM.png)
- [Screenshot 2026-10-23 at 12.08.06 PM.png](attachments/Screenshot%202026-10-23%20at%2012.08.06%20PM.png)
- [Screenshot 2026-10-23 at 12.08.17 PM.png](attachments/Screenshot%202026-10-23%20at%2012.08.17%20PM.png)
- [Screenshot 2026-10-23 at 12.08.25 PM.png](attachments/Screenshot%202026-10-23%20at%2012.08.25%20PM.png)
