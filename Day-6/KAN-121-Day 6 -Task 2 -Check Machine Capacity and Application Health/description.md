# KAN-121: Day 6 |Task 2 |Check Machine Capacity and Application Health

- **Jira:** https://sasidharana504.atlassian.net/browse/KAN-121
- **Status:** Review
- **Assignee:** sasidharana504
- **Issue type:** Task
- **Priority:** Medium
- **Resolution:** —
- **Reporter:** pranavi selvaraju
- **Created:** 2026-10-18T17:28:03.384Z
- **Updated:** 2026-10-19T16:08:57.473Z
- **Due date:** —
- **Labels:** —
- **Components:** —

## Description

deployment.

Steps:

 (1) Connect to the assigned Linux host. 

(2) Identify the OS.

 (3) inspect disk, memory, and running processes.

 (4) Install Nginx. 

(5) Validate its configuration and service.

 (6) Check port 80 and HTTP response. 

(7) Inspect logs. 

(8) Record findings.

cat /etc/os-release
lsb_release -a   # if installed
df -h
free -h
top
sudo apt update && sudo apt install nginx -y
sudo nginx -t
sudo systemctl status nginx
sudo ss -lntp | grep ':80'
curl -s -o /dev/null -w '%{http_code}\n' http://localhost

Log checks on systemd systems:

sudo journalctl -u nginx -n 50
sudo ls -lh /var/log/nginx/
sudo tail -20 /var/log/nginx/access.log

OS-specific note: Ubuntu/Debian package and systemd commands are normally available.

Expected outcome: OS and resource information recorded; Nginx configuration and service checked; port 80 and HTTP response tested; logs inspected; health-check report attached.

## Attachments

- [Screenshot 2026-10-16 at 4.12.47 PM.png](attachments/Screenshot%202026-10-16%20at%204.12.47%20PM.png)
- [Screenshot 2026-10-16 at 4.21.29 PM.png](attachments/Screenshot%202026-10-16%20at%204.21.29%20PM.png)
