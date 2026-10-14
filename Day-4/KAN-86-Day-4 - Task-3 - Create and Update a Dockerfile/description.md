# KAN-86: Day-4 | Task-3 | Create and Update a Dockerfile

- **Jira:** https://sasidharana504.atlassian.net/browse/KAN-86
- **Status:** To Do
- **Assignee:** sasidharana504
- **Issue type:** Task
- **Priority:** Medium
- **Resolution:** —
- **Reporter:** sasidharana504
- **Created:** 2026-10-14T10:35:20.823Z
- **Updated:** 2026-10-14T10:53:37.566Z
- **Due date:** —
- **Labels:** —
- **Components:** —

## Description

Create a Dockerfile based on Ubuntu that installs vim, wget, and unzip. Then create a second image using the first image as its base, uninstall unzip, and install PHP CLI. Build separate image versions and verify the installed utilities.

Part 1: Create the Initial Dockerfile (V1)

Create a file named Dockerfile with the following content:


```
FROM ubuntu:24.04

RUN apt-get update && apt-get install -y vim wget unzip \
    && rm -rf /var/lib/apt/lists/*

CMD ["bash"]
```

Build the image:


```
docker build -t custom-ubuntu:v1 .
```

Run the container:


```
docker run -it --name ubuntu-v1 custom-ubuntu:v1
```

Verify the installed utilities:


```
vim --version
wget --version
unzip -v
```

Exit the container:


```
exit
```

Part 2: Update the Dockerfile (V2)

Open the Dockerfile using vi:


```
vi Dockerfile
```

Replace its contents with:


```
FROM custom-ubuntu:v1

RUN apt-get purge -y unzip \
    && apt-get update && apt-get install -y php-cli \
    && rm -rf /var/lib/apt/lists/*

CMD ["bash"]
```

Build the updated image:


```
docker build -t custom-ubuntu:v2 .
```

Run the updated container:


```
docker run -it --name ubuntu-v2 custom-ubuntu:v2
```

Verify the installed utilities:


```
vi --version
wget --version
php --version
command -v unzip
```

The final command should produce no output if unzip is no longer available.

Exit the container:


```
exit
```

Acceptance Criteria

- Create a valid Dockerfile based on Ubuntu 24.04.
- Build V1 with vim, wget, and unzip.
- Verify that all three utilities are installed in V1.
- Build V2 using custom-ubuntu:v1 as its base image.
- Uninstall unzip and install PHP CLI in V2.
- Verify that vi, wget, and PHP are available in V2.
- Confirm that unzip is no longer available in V2.
- Capture screenshots of both Dockerfile versions, build outputs, and verification commands.
Cleanup

Remove the containers and custom images after capturing screenshots:


```
docker rm -f ubuntu-v1 ubuntu-v2
docker rmi custom-ubuntu:v2 custom-ubuntu:v1
```

Verify cleanup:


```
docker ps -a
docker images
```

Notes

- Run all build commands from the directory containing the Dockerfile.
- V2 inherits the packages installed in V1, so vim and wget do not need to be reinstalled.
- The CMD ["bash"] instruction uses Docker's exec form.
- Use separate image tags (v1 and v2) to distinguish the two versions.
- The cleanup commands remove the containers and custom images but leave the base Ubuntu image available locally.

## Attachments

- [Screenshot 2026-10-14 at 4.08.16 PM.png](attachments/Screenshot%202026-10-14%20at%204.08.16%20PM.png)
- [Screenshot 2026-10-14 at 4.09.55 PM.png](attachments/Screenshot%202026-10-14%20at%204.09.55%20PM.png)
- [Screenshot 2026-10-14 at 4.11.11 PM.png](attachments/Screenshot%202026-10-14%20at%204.11.11%20PM.png)
- [Screenshot 2026-10-14 at 4.11.23 PM.png](attachments/Screenshot%202026-10-14%20at%204.11.23%20PM.png)
- [Screenshot 2026-10-14 at 4.11.37 PM.png](attachments/Screenshot%202026-10-14%20at%204.11.37%20PM.png)
- [Screenshot 2026-10-14 at 4.19.20 PM.png](attachments/Screenshot%202026-10-14%20at%204.19.20%20PM.png)
- [Screenshot 2026-10-14 at 4.21.41 PM.png](attachments/Screenshot%202026-10-14%20at%204.21.41%20PM.png)
- [Screenshot 2026-10-14 at 4.21.56 PM.png](attachments/Screenshot%202026-10-14%20at%204.21.56%20PM.png)
- [Screenshot 2026-10-14 at 4.22.39 PM.png](attachments/Screenshot%202026-10-14%20at%204.22.39%20PM.png)
- [Screenshot 2026-10-14 at 4.23.14 PM.png](attachments/Screenshot%202026-10-14%20at%204.23.14%20PM.png)
