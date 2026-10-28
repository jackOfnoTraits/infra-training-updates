# DC-2: Day-10 - Task 1 - Practice 10 Linux Data Analysis Commands

- **Jira:** https://lakshmibanka516.atlassian.net/browse/DC-2
- **Status:** Done
- **Assignee:** sasidharana504
- **Issue type:** Story
- **Priority:** Medium
- **Resolution:** Done
- **Reporter:** Banka Lakshmi
- **Created:** 2026-10-26T09:58:09.169Z
- **Updated:** 2026-10-26T16:25:12.184Z
- **Due date:** —
- **Labels:** —
- **Components:** —

## Description

Labels: linux, devops, command-line, data-analysis, hands-on-practice

Description

As part of Linux and DevOps upskilling, practice 10 essential Linux command-line tools used for data processing, log analysis, text manipulation, dataset splitting, and performance measurement.

Set up a Linux environment using Multipass and work with sample sales CSV data and application/access logs. Execute each command, understand its purpose, and document the results.

Objectives

- Develop proficiency in Linux text-processing and data-analysis commands.
- Analyze application logs to identify errors, warnings, HTTP failures, and repeated events.
- Process CSV datasets using command-line tools.
- Split large files into manageable chunks.
- Measure command execution time and compare performance.
Scope: 10 Commands


# | Command | Practice Activity
1 | awk | Calculate statistics and extract fields from CSV and log files.
2 | datamash | Calculate mean, median, minimum, and maximum sales values.
3 | sort and uniq | Sort records and identify repeated values or IP addresses.
4 | join | Combine two datasets using a common key.
5 | sed | Search, replace, and transform text in files.
6 | grep | Find HTTP errors, application exceptions, warnings, and specific requests.
7 | wc | Count lines, words, and bytes in datasets and log files.
8 | paste | Combine corresponding lines from multiple files.
9 | split | Divide large CSV or log files into smaller chunks.
10 | time | Measure command execution time for sorting, searching, and processing large files.

Environment and Prerequisites

- A working Multipass Linux VM.
- Sample files: sales.csv, access.log, application.log, sales_large.csv, and application_large.log.
- Required utilities: awk, sed, grep, sort, uniq, wc, paste, split, and time.
- Install datamash if it is unavailable.
- Transfer the practice datasets from the host machine into the VM.
Implementation Steps

1. Create a dedicated practice directory inside the Linux VM.
2. Transfer and verify all sample datasets.
3. Execute each of the 10 commands against the relevant files.
4. Record the commands used and explain their output.
5. Analyze access logs for HTTP status codes 4xx and 5xx.
6. Analyze application logs for ERROR and WARN entries.
7. Use split to divide the large dataset into chunks and verify the resulting files.
8. Use time to benchmark multiple operations on the large datasets.
9. Document observations, errors encountered, and lessons learned.

## Attachments

- [Screenshot 2026-10-26 at 9.46.39 PM.png](attachments/Screenshot%202026-10-26%20at%209.46.39%20PM.png)
- [Screenshot 2026-10-26 at 9.46.53 PM.png](attachments/Screenshot%202026-10-26%20at%209.46.53%20PM.png)
- [Screenshot 2026-10-26 at 9.47.09 PM.png](attachments/Screenshot%202026-10-26%20at%209.47.09%20PM.png)
- [Screenshot 2026-10-26 at 9.47.29 PM.png](attachments/Screenshot%202026-10-26%20at%209.47.29%20PM.png)
- [Screenshot 2026-10-26 at 9.47.44 PM.png](attachments/Screenshot%202026-10-26%20at%209.47.44%20PM.png)
- [Screenshot 2026-10-26 at 9.48.08 PM.png](attachments/Screenshot%202026-10-26%20at%209.48.08%20PM.png)
- [Screenshot 2026-10-26 at 9.48.25 PM.png](attachments/Screenshot%202026-10-26%20at%209.48.25%20PM.png)
