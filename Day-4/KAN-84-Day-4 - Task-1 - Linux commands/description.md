# KAN-84: Day-4 | Task-1 | Linux commands

- **Jira:** https://sasidharana504.atlassian.net/browse/KAN-84
- **Status:** Review
- **Assignee:** sasidharana504
- **Issue type:** Task
- **Priority:** Medium
- **Resolution:** —
- **Reporter:** sasidharana504
- **Created:** 2026-10-14T10:13:33.279Z
- **Updated:** 2026-10-14T10:24:16.190Z
- **Due date:** —
- **Labels:** —
- **Components:** —

## Description

Theme: Process Management & Linux Administration

Today's commands focus on managing processes, inspecting resource usage, monitoring open files, checking user identities, and understanding process signals.

Today's Toolkit

1. pgrep -a bash — Find running Bash processes and display their process IDs and command lines.
2. pstree -p — Display running processes in a tree structure with their PIDs.
3. vmstat 1 5 — Monitor memory, CPU activity, processes, and I/O statistics over five intervals.
4. iostat -xz 1 3 — Inspect CPU and detailed disk I/O performance statistics. (Install sysstat if unavailable.)
5. lsof +D /tmp — List open files under /tmp and identify which processes are using them.
6. fuser -v /tmp — Identify processes accessing the /tmp directory.
7. id — Display your user ID, primary group, and supplementary group memberships.
8. getent passwd — Query the system's configured user account database.
9. systemctl --failed — List systemd units currently in a failed state.
10. kill -l — Display the signal names and numbers supported by your system.
Notes

- iostat and lsof may require installing packages such as sysstat and lsof.
- lsof +D /tmp can take some time if the directory contains many files.
- These commands are primarily diagnostic and do not intentionally modify system configuration or terminate processes.

## Attachments

- [Screenshot 2026-10-14 at 3.44.28 PM.png](attachments/Screenshot%202026-10-14%20at%203.44.28%20PM.png)
- [Screenshot 2026-10-14 at 3.49.19 PM.png](attachments/Screenshot%202026-10-14%20at%203.49.19%20PM.png)
- [Screenshot 2026-10-14 at 3.49.37 PM.png](attachments/Screenshot%202026-10-14%20at%203.49.37%20PM.png)
- [Screenshot 2026-10-14 at 3.49.48 PM.png](attachments/Screenshot%202026-10-14%20at%203.49.48%20PM.png)
- [Screenshot 2026-10-14 at 3.50.06 PM.png](attachments/Screenshot%202026-10-14%20at%203.50.06%20PM.png)
