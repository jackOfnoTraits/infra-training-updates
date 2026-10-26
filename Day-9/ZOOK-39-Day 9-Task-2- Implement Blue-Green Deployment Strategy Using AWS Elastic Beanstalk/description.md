# ZOOK-39: Day 9-Task-2: Implement Blue-Green Deployment Strategy Using AWS Elastic Beanstalk

- **Jira:** https://gomathiboyalla4-1792569022463.atlassian.net/browse/ZOOK-39
- **Status:** In review
- **Assignee:** sasidharana504
- **Issue type:** Task
- **Priority:** Medium
- **Resolution:** —
- **Reporter:** Boyalla Gomathi
- **Created:** 2026-10-24T08:56:55.903Z
- **Updated:** 2026-10-25T06:27:26.826Z
- **Due date:** —
- **Labels:** —
- **Components:** —

## Description

Description:

As part of our deployment and release engineering upskilling, this task focuses on implementing a Blue-Green Deployment strategy using AWS Elastic Beanstalk. The objective is to maintain two separate application environments, Blue (current production version) and Green (updated application version), to enable controlled releases, validate changes before switching traffic, and minimize application downtime during deployments.

Create two Elastic Beanstalk environments, deploy the initial application to Blue, deploy an updated version to Green, validate the changes through the Green environment URL, and perform an environment URL/domain swap to direct traffic to the updated application.

Blue-Green Deployment Challenges

1. AWS Elastic Beanstalk Application Setup

- Concept: Create an Elastic Beanstalk application that manages separate environments for the current and updated application versions.
- Practice:  - Create an Elastic Beanstalk application. - Select the appropriate platform and runtime for the application. - Prepare a simple web application with a visible version identifier.
2. Create the Blue Environment

- Concept: Deploy the initial stable application version into the Blue environment, representing the current production release.
- Practice:  - Create an Elastic Beanstalk environment named blue-env. - Deploy the initial application version, such as v1. - Access the Blue environment URL and verify that the application is working correctly. - Record the environment URL and the displayed application version.
3. Create the Green Environment

- Concept: Establish a separate environment for deploying and validating the next application release without immediately affecting the Blue environment.
- Practice:  - Create another Elastic Beanstalk environment named green-env. - Use the same application platform and compatible configuration as Blue. - Deploy the initial version or a baseline application. - Verify that Green is healthy and accessible through its environment URL.
4. Update the Green Environment

- Concept: Deploy a new application version to Green while keeping Blue unchanged and available.
- Practice:  - Modify the webpage to display an updated version identifier, such as v2. - Update the webpage content with a visible change, such as a new heading or release message. - Deploy the updated application bundle to green-env. - Confirm that the Green environment displays the new version while Blue continues to display v1.
5. Validate the Green Environment

- Concept: Test the updated application before routing production traffic to it.
- Practice:  - Open the Green environment URL in a browser. - Verify that the updated webpage and version identifier are visible. - Check application health, HTTP responses, and relevant logs. - Confirm that the updated environment is ready to receive production traffic.
6. Perform the Environment URL Swap

- Concept: Use Elastic Beanstalk's environment swap functionality to exchange the environment URLs, directing the existing production URL to the updated application.
- Practice:  - Navigate to the Elastic Beanstalk environment management console. - Select the environment URL swap action between blue-env and green-env. - Confirm the swap and wait for the operation to complete. - Verify that the original Blue URL now serves the updated application from Green. - Record the environment URLs before and after the swap.
7. Verify the Deployment After the Swap

- Concept: Confirm that the updated application is accessible through the production-facing URL after the traffic switch.
- Practice:  - Open the original Blue environment URL in a browser. - Verify that the webpage displays version v2 and the updated content. - Open the other environment URL and record which application version it serves. - Check HTTP responses and environment health. - Capture screenshots showing the updated webpage through the original production URL.
8. Validate Blue-Green Isolation and Availability

- Concept: Ensure that the environment switch does not unintentionally modify the previous application deployment or introduce availability issues.
- Practice:  - Confirm that the original Blue deployment remains available in the other environment after the swap. - Check both environments for health and application errors. - Verify that the production-facing URL consistently serves the expected version. - Document any downtime, DNS caching, or temporary routing inconsistencies observed.
Acceptance Criteria

- Two separate Elastic Beanstalk environments, blue-env and green-env, are created successfully.
- The Blue environment initially serves application version v1.
- The Green environment is updated to version v2 without modifying the Blue application's deployment.
- The Green environment is validated before the URL swap.
- The Elastic Beanstalk environment URL swap completes successfully.
- The original Blue environment URL serves the updated v2 webpage after the swap.
- The final environment URLs, application versions, and health statuses are documented.
- Before-and-after screenshots are attached as execution evidence.
- Any deployment issues and rollback considerations are documented.
Deliverable: A working Blue-Green deployment demonstration on AWS Elastic Beanstalk, supported by environment URLs, version verification, health checks, and before-and-after screenshots.

Environment: AWS Elastic Beanstalk

Labels: aws, elastic-beanstalk, blue-green-deployment, ci-cd, deployment, release-engineering

## Attachments

- [Screenshot 2026-10-25 at 11.35.06 AM.png](attachments/Screenshot%202026-10-25%20at%2011.35.06%20AM.png)
- [Screenshot 2026-10-25 at 11.39.37 AM.png](attachments/Screenshot%202026-10-25%20at%2011.39.37%20AM.png)
- [Screenshot 2026-10-25 at 11.39.56 AM.png](attachments/Screenshot%202026-10-25%20at%2011.39.56%20AM.png)
- [Screenshot 2026-10-25 at 11.43.46 AM.png](attachments/Screenshot%202026-10-25%20at%2011.43.46%20AM.png)
- [Screenshot 2026-10-25 at 11.44.45 AM.png](attachments/Screenshot%202026-10-25%20at%2011.44.45%20AM.png)
- [Screenshot 2026-10-25 at 11.45.12 AM.png](attachments/Screenshot%202026-10-25%20at%2011.45.12%20AM.png)
- [Screenshot 2026-10-25 at 11.53.54 AM.png](attachments/Screenshot%202026-10-25%20at%2011.53.54%20AM.png)
- [Screenshot 2026-10-25 at 11.54.05 AM.png](attachments/Screenshot%202026-10-25%20at%2011.54.05%20AM.png)
- [Screenshot 2026-10-25 at 11.55.18 AM.png](attachments/Screenshot%202026-10-25%20at%2011.55.18%20AM.png)
- [Screenshot 2026-10-25 at 11.55.28 AM.png](attachments/Screenshot%202026-10-25%20at%2011.55.28%20AM.png)
- [Screenshot 2026-10-25 at 11.56.41 AM.png](attachments/Screenshot%202026-10-25%20at%2011.56.41%20AM.png)
