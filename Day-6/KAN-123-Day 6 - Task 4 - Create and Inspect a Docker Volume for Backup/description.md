# KAN-123: Day 6 | Task 4 | Create and Inspect a Docker Volume for Backup

- **Jira:** https://sasidharana504.atlassian.net/browse/KAN-123
- **Status:** Review
- **Assignee:** sasidharana504
- **Issue type:** Task
- **Priority:** Medium
- **Resolution:** —
- **Reporter:** pranavi selvaraju
- **Created:** 2026-10-18T17:34:32.732Z
- **Updated:** 2026-10-19T16:15:41.625Z
- **Due date:** —
- **Labels:** —
- **Components:** —

## Description

Objective: Create a named volume and prove that data remains available after the original container is deleted.

docker volume create my-vol
docker volume ls
docker inspect my-vol
docker inspect -f "{{ .Mountpoint }}" my-vol

Mount the volume in an Ubuntu container:

docker run -dit --name backup-container --mount source=my-vol,target=/data ubuntu:22.04
docker exec backup-container bash -c 'echo "Docker volume backup test" > /data/samplefile'
docker exec backup-container ls -l /data
docker exec backup-container cat /data/samplefile

Remove the container but retain the volume, then attach it to a new container:

docker rm -f backup-container
docker run -dit --name backup-container-2 --mount source=my-vol,target=/data ubuntu:22.04
docker exec backup-container-2 cat /data/samplefile

Expected outcome: Volume is created and inspected, sample file is readable, and its contents remain after container recreation. Do not delete my-vol during the test.

## Attachments

- [Screenshot 2026-10-16 at 3.36.16 PM.png](attachments/Screenshot%202026-10-16%20at%203.36.16%20PM.png)
- [Screenshot 2026-10-16 at 3.36.24 PM.png](attachments/Screenshot%202026-10-16%20at%203.36.24%20PM.png)
- [Screenshot 2026-10-16 at 3.36.34 PM.png](attachments/Screenshot%202026-10-16%20at%203.36.34%20PM.png)
- [Screenshot 2026-10-19 at 9.45.13 PM.png](attachments/Screenshot%202026-10-19%20at%209.45.13%20PM.png)
