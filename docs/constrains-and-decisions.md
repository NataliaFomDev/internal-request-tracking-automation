# Constraints and Design Decisions

## Constraint

The available automation tier imposed limits on how the workflow could update and synchronize records across all tools within a single automation flow.

## Decision

Instead of forcing a fragile all-in-one workflow, the solution was split into two separate automation flows:

1. intake workflow
2. completion workflow

## Why this worked

This design improved reliability and made the automation easier to maintain while still covering the full request lifecycle:
- request capture
- task creation
- completion event handling
- completion reporting

## Trade-off

The final completion data was written to a dedicated reporting sheet rather than appended back into the original intake sheet.

## Why this was acceptable

The main business need was not a perfectly unified table, but a reliable process that provided:
- visibility into submitted requests
- a clear execution flow
- completion history
- date and responsible person for finished work

## Practical result

Even under platform constraints, the solution achieved the intended operational outcome:
- less manual coordination
- better tracking of request status
- structured completion log
- continued day-to-day usefulness for employees