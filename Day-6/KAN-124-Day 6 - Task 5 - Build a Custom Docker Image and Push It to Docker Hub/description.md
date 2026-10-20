# KAN-124: Day 6 | Task 5 |  Build a Custom Docker Image and Push It to Docker Hub

- **Jira:** https://sasidharana504.atlassian.net/browse/KAN-124
- **Status:** Review
- **Assignee:** sasidharana504
- **Issue type:** Task
- **Priority:** Medium
- **Resolution:** —
- **Reporter:** pranavi selvaraju
- **Created:** 2026-10-18T17:35:16.481Z
- **Updated:** 2026-10-19T16:16:36.160Z
- **Due date:** —
- **Labels:** —
- **Components:** —

## Description

Objective: Build, tag, publish, and pull a custom image.

mkdir -p custom-image && cd custom-image
vi Dockerfile

Dockerfile:

FROM ubuntu:22.04
RUN apt-get update && apt-get install -y curl vim && \
    rm -rf /var/lib/apt/lists/*
CMD ["bash"]

docker build -t my-custom-image:v1.0 .
docker images
docker login
docker tag my-custom-image:v1.0 YOUR_DOCKERHUB_USERNAME/my-custom-image:v1.0
docker push YOUR_DOCKERHUB_USERNAME/my-custom-image:v1.0
docker pull YOUR_DOCKERHUB_USERNAME/my-custom-image:v1.0
docker images

Replace YOUR_DOCKERHUB_USERNAME with the actual account name. Use a personal access token if required. Never place passwords, tokens, or private keys in an image or screenshot.

Expected outcome: Custom image is built, tagged, pushed, and pulled successfully. Attach the repository URL and evidence.

## Attachments

- [Screenshot 2026-10-16 at 3.55.39 PM.png](attachments/Screenshot%202026-10-16%20at%203.55.39%20PM.png)
- [Screenshot 2026-10-16 at 3.58.50 PM.png](attachments/Screenshot%202026-10-16%20at%203.58.50%20PM.png)
- [Screenshot 2026-10-16 at 3.58.58 PM.png](attachments/Screenshot%202026-10-16%20at%203.58.58%20PM.png)
- [Screenshot 2026-10-16 at 3.59.18 PM.png](attachments/Screenshot%202026-10-16%20at%203.59.18%20PM.png)
