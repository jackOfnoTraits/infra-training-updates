# DC-18: Day-11 - Task 1 - Practice 10 Linux Commands for Data Cleaning and Preprocessing

- **Jira:** https://lakshmibanka516.atlassian.net/browse/DC-18
- **Status:** Done
- **Assignee:** sasidharana504
- **Issue type:** Task
- **Priority:** Medium
- **Resolution:** Done
- **Reporter:** sasidharana504
- **Created:** 2026-10-27T06:31:05.280Z
- **Updated:** 2026-10-28T04:39:24.108Z
- **Due date:** —
- **Labels:** —
- **Components:** —

## Description

Description

Practice 10 Linux command-line techniques for inspecting, cleaning, validating, transforming, comparing, and compressing structured datasets.

The 10 Command Challenges

1. jq — JSONL Filtering

Filter records with missing customer IDs and save the valid records separately.


```
jq -c 'select(.customer_id != null)' messy_events.jsonl \
  > data_pipeline/cleaned/valid_events.jsonl
```

2. awk — Invalid Record Detection

Identify sales records with missing or negative quantities.


```
awk -F, 'NR>1 && ($3=="" || $3<0)' \
  data_pipeline/raw/sales.csv
```

3. sort — Record Sorting

Sort JSONL records to prepare for comparison.


```
sort messy_events.jsonl \
  > data_pipeline/cleaned/sorted_events.jsonl
```

4. uniq — Duplicate Detection

Identify identical repeated records.


```
sort messy_events.jsonl | uniq -cd
```

5. comm — Dataset Comparison

Compare sorted raw and cleaned datasets to identify removed records.


```
comm -23 \
  <(sort messy_events.jsonl) \
  <(sort data_pipeline/cleaned/valid_events.jsonl)
```

6. csvstat — Data Profiling

Inspect column types, null values, unique values, and numeric distributions.


```
csvstat data_pipeline/raw/sales.csv
```

7. in2csv — Format Conversion

Convert the JSON array into CSV format.


```
in2csv --format json messy_events.json \
  > data_pipeline/cleaned/events.csv
```

8. csvclean — CSV Validation

Check the converted CSV for structural issues.


```
csvclean -n data_pipeline/cleaned/events.csv
```

9. zcat — Compressed Data Inspection

Inspect compressed CSV contents without extracting the file.


```
zcat messy_events.csv.gz | head -n 10
```

10. gzip — Data Compression

Compress the cleaned CSV while retaining the original.


```
gzip -k data_pipeline/cleaned/events.csv
```

Acceptance Criteria

- Execute all 10 command challenges successfully.
- Filter JSONL records with missing customer IDs.
- Identify missing and negative quantities in the sales dataset.
- Sort datasets and detect duplicate lines.
- Compare raw and cleaned datasets and identify removed records.
- Profile the sales dataset using csvstat.
- Convert JSON to CSV using in2csv.
- Validate CSV structure using csvclean.
- Inspect compressed data using zcat.
- Compress the cleaned CSV using gzip -k.
- Preserve raw datasets and verify output record counts.
- Document command outputs and findings using terminal evidence.
Deliverables

- Cleaned JSONL and CSV files.
- Invalid-record and duplicate-detection results.
- CSV profiling and validation outputs.
- Compressed CSV artifact.
- Terminal screenshots or command logs.
- A brief report describing the data-quality issues found and the cleaning decisions made.
Definition of Done

All 10 command challenges are completed, output files are verified, raw datasets remain unchanged, and the preprocessing results are documented for review.

Prerequisite: Install jq, csvkit (for csvstat, in2csv, and csvclean), and standard GNU/Linux utilities. The JSON input for in2csv --format json must be a valid JSON document, such as an array created from JSONL using jq -s '.'.

## Attachments

- [Screenshot 2026-10-27 at 9.29.59 PM.png](attachments/Screenshot%202026-10-27%20at%209.29.59%20PM.png)
- [Screenshot 2026-10-27 at 9.30.20 PM.png](attachments/Screenshot%202026-10-27%20at%209.30.20%20PM.png)
- [Screenshot 2026-10-27 at 9.30.51 PM.png](attachments/Screenshot%202026-10-27%20at%209.30.51%20PM.png)
- [Screenshot 2026-10-27 at 9.31.26 PM.png](attachments/Screenshot%202026-10-27%20at%209.31.26%20PM.png)
- [Screenshot 2026-10-27 at 9.35.39 PM.png](attachments/Screenshot%202026-10-27%20at%209.35.39%20PM.png)
- [Screenshot 2026-10-27 at 9.40.46 PM.png](attachments/Screenshot%202026-10-27%20at%209.40.46%20PM.png)
- [Screenshot 2026-10-27 at 9.44.54 PM.png](attachments/Screenshot%202026-10-27%20at%209.44.54%20PM.png)
- [Screenshot 2026-10-27 at 9.54.05 PM.png](attachments/Screenshot%202026-10-27%20at%209.54.05%20PM.png)
