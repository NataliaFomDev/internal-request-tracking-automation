# Future Improvements

## 1. Move the workflow to a more flexible automation layer

A future version of the solution could be implemented in n8n or a similar workflow platform with fewer structural limitations. This would allow the process to be managed in a more unified and maintainable way.

## 2. Consolidate request lifecycle tracking into a single source of truth

Instead of splitting request intake and completion history across separate sheets, the workflow could be redesigned around a single operational table keyed by request ID.

This would make it easier to:
- find and update the original request record
- keep the full lifecycle in one place
- simplify reporting logic
- reduce data duplication

## 3. Update completion data directly by request ID

With a unified storage structure, the completion workflow could locate the original request by request ID and update fields such as:
- completion date
- completion status
- responsible person
- comments or resolution notes

## 4. Improve reporting for managers

A next iteration could include automated reporting for team leads or department managers, for example:
- completed requests by executor
- completion time trends
- overdue or aging requests
- workload distribution
- daily or weekly summary reports

## 5. Add notification scenarios

The workflow could be extended with notifications such as:
- new request assigned
- request overdue
- request completed
- daily digest of open items

## 6. Add stronger process monitoring

A more advanced version could include:
- failed automation tracking
- retry logic
- missing data checks
- operational logs for troubleshooting

## 7. Improve data structure for analytics

The reporting layer could be expanded to support:
- executor performance summaries
- request type trends
- processing time by category
- completion volume over time

## Summary

The current solution already delivers practical value and supports day-to-day operations. A future redesign would focus on unifying the data model, reducing fragmentation, and improving reporting, maintainability, and process visibility.