# KAN-40: Day-2-Infra Task 2 (Linux Filesystem Permissions)

- **Jira:** https://sasidharana504.atlassian.net/browse/KAN-40
- **Status:** Done
- **Assignee:** sasidharana504
- **Issue type:** Task
- **Priority:** Medium
- **Resolution:** Done
- **Reporter:** sasidharana504
- **Created:** 2026-10-12T10:00:15.162Z
- **Updated:** 2026-10-12T13:00:11.363Z
- **Due date:** —
- **Labels:** —
- **Components:** —

## Description

Description: Proper access control is the backbone of Linux security. Today's mission is to move beyond basic chmod +x and master symbolic modes, octal values, ownership manipulation.

Set up a practice directory (mkdir perm_sandbox && cd perm_sandbox) and work through the following 5 core concepts and commands.

1. Inspecting Detailed Permission Structures (ls -l & stat)

- Concept: Unpack the 10-character permission string (-rwxr-xr-x) and inode metadata.
- Practice: Create a test file (touch test.txt) and run ls -l test.txt and stat test.txt.
- Deep-Dive: Understand the segments: File type (- for file, d for directory), Owner (u), Group (g), and Others (o).
2. Symbolic Mode Modification (chmod u=rwx,g=rx,o=r)

- Concept: Modify permissions explicitly using letters (u, g, o, a) and operators (+, -, =).
- Practice:  - Grant execute permission to everyone: chmod a+x test.txt - Remove write access for others: chmod o-w test.txt - Set exact permissions for owner only: chmod u=rw,g=,o= test.txt
3. Octal / Numeric Mode (Base-8 Permissions: 775, 644)

- Concept: Use numeric representations where Read = 4, Write = 2, and Execute = 1.
- Practice:  - Apply standard secure file permissions (rw-r--r--): chmod 644 test.txt - Apply standard secure directory permissions (rwxr-xr-x): chmod 755 . - Apply restricted private permissions (rwx------): chmod 700 test.txt
4. Recursive Permission Enforcement (chmod -R)

- Concept: Apply permission changes recursively down an entire directory tree.
- Practice: Create a nested structure (mkdir -p a/b/c && touch a/b/c/file.txt), then lock down the tree: chmod -R 750 a/.
5. Ownership and Group Reassignment (chown & chgrp)

- Concept: Manage who owns the file and which secondary group has access rights.
- Practice:  - Change file owner: sudo chown $USER test.txt - Change owner and group simultaneously: sudo chown $USER:$USER test.txt - Change group only: sudo chgrp adm test.txt

## Attachments

- [Screenshot 2026-10-12 at 6.09.31 PM.png](attachments/Screenshot%202026-10-12%20at%206.09.31%20PM.png)
- [Screenshot 2026-10-12 at 6.11.53 PM.png](attachments/Screenshot%202026-10-12%20at%206.11.53%20PM.png)
- [Screenshot 2026-10-12 at 6.13.55 PM.png](attachments/Screenshot%202026-10-12%20at%206.13.55%20PM.png)
- [Screenshot 2026-10-12 at 6.14.42 PM.png](attachments/Screenshot%202026-10-12%20at%206.14.42%20PM.png)
- [Screenshot 2026-10-12 at 6.16.10 PM.png](attachments/Screenshot%202026-10-12%20at%206.16.10%20PM.png)
- [Screenshot 2026-10-12 at 6.18.44 PM.png](attachments/Screenshot%202026-10-12%20at%206.18.44%20PM.png)
