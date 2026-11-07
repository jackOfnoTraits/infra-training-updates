### Day 19 – Task 2: Power BI Performance Optimization

**Tool Used:** Power BI Performance Analyzer

**Activities Performed:**

- Enabled Performance Analyzer from the Optimize/View tab.
- Started recording report performance.
- Refreshed all dashboard visuals.
- Examined individual visual loading durations.
- Exported the Performance Analyzer trace as JSON.
- Tested dashboard responsiveness by changing slicer selections.
- Compared initial refresh performance with interactive filtering performance.

**Observations:**

The initial dashboard refresh recorded visual loading durations between approximately 559 ms and 664 ms for the primary visuals.

Profit by Product Category was the slowest visual during the initial refresh, taking approximately 664 ms.

During slicer interactions, some visuals experienced higher execution times, with the slowest recorded visual taking approximately 1,171 ms.

The detailed trace indicated that query execution contributed more to the loading time than visual rendering.

**Findings:**

- Initial dashboard performance was satisfactory.
- Visual rendering was relatively quick.
- Query execution was the primary area requiring further investigation.
- Slicer interactions introduced additional processing overhead.

**Conclusion:**

Performance Analyzer successfully helped identify visual-level performance characteristics and potential bottlenecks. The dashboard demonstrated acceptable initial loading performance, although further optimization of query execution and filter interactions could improve responsiveness.
