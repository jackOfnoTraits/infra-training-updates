# KAN-109: DAY-5 |TASK -1 | LINUX COMMANDS

- **Jira:** https://sasidharana504.atlassian.net/browse/KAN-109
- **Status:** Review
- **Assignee:** sasidharana504
- **Issue type:** Task
- **Priority:** Medium
- **Resolution:** —
- **Reporter:** sasidharana504
- **Created:** 2026-10-15T07:57:02.008Z
- **Updated:** 2026-10-15T12:14:36.932Z
- **Due date:** —
- **Labels:** —
- **Components:** —

## Description

These are the common commands they should know and use during implementation.

Task Title: Learn and Practise 10 New Linux Commands

Description:

Research and practise 10 Linux commands that are not commonly used in daily work. Understand their syntax, options, use cases, and practical applications in system administration and troubleshooting.




```
# 1. Find all .log files
find /var/log -type f -name "*.log" 2>/dev/null

# 2. Search logs for errors
grep -in "error" application.log

# 3. Display the first column of a file
awk '{print $1}' data.txt

# 4. Replace text in a file's output
sed 's/ERROR/WARNING/g' application.log

# 5. Process a list of files
printf '%s\n' *.log | xargs -r grep -n "failed"

# 6. Create a compressed archive
tar -czf logs.tar.gz logs/

# 7. Find large directories
du -sh /var/log/* 2>/dev/null

# 8. Check which process uses port 8080
lsof -i :8080

# 9. View recent system logs
journalctl -n 50

# 10. Monitor memory usage every 2 seconds
watch -n 2 free -h
```

## Attachments

- [Screenshot 2026-10-15 at 1.33.17 PM.png](attachments/Screenshot%202026-10-15%20at%201.33.17%20PM.png)
- [Screenshot 2026-10-15 at 1.33.32 PM.png](attachments/Screenshot%202026-10-15%20at%201.33.32%20PM.png)
- [Screenshot 2026-10-15 at 1.33.41 PM.png](attachments/Screenshot%202026-10-15%20at%201.33.41%20PM.png)
