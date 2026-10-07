\# Task Tracker Patch Notes



\## Summary of changes



\* Fixed the task search SQL in `TaskRepository` by grouping title/description search conditions so the archived and status filters apply correctly to all search matches.

\* Removed an artificial `Thread.sleep()` delay from `TaskController` that unnecessarily slowed API requests based on query length.

\* Updated `App.jsx` so changing the search text or status filter resets pagination to page 1.



\## What I did not change and why



\* I did not modify the Oracle PL/SQL reference artifact because the local application uses the Spring Data repository with H2, and the assignment asked for focused changes.

\* I did not change unrelated warnings, dependency audit findings, or database ID ordering because they were outside the highest-value bugs identified during testing.



\## Biggest remaining risk



\* Pagination currently loads all matching tasks and then selects the requested page in memory. This is acceptable for the assignment dataset, but it would not scale well for a large production dataset.



\## Tools / AI used



\* Used ChatGPT/AI to inspect the code, identify the SQL operator-precedence issue, reason about the pagination behavior, and review focused fixes.

\* Verified the changes manually through the application UI and API requests, and reviewed the final Git diff.



