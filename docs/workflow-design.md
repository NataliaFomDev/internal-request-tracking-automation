# Workflow Design

## Overview

The solution is intentionally split into two workflows to support a complete request lifecycle while keeping the automation maintainable and reliable.

## Workflow 1: Request intake and task creation

### Trigger
A user submits a request through a form.

### Input
Structured request data is captured in the intake sheet.

### Automation steps
- detect new request submission
- read structured request data
- create a task in the task board
- preserve request intake record in the spreadsheet

### Outcome
Each submitted request becomes a tracked execution item in the task board.

## Workflow 2: Completion tracking and reporting

### Trigger
A task is moved to a completion state in the task board.

### Input
Task completion event and task metadata.

### Automation steps
- detect task completion state
- extract relevant completion data
- write completion record into a reporting-oriented sheet
- preserve execution date and responsible person

### Outcome
Completed work is recorded in a dedicated completion log for visibility and reporting.

## Why two workflows

The split design improved:
- reliability
- maintainability
- separation of concerns
- practical handling of platform limitations

## Lifecycle coverage

The combined design captures the full path:
- request submitted
- task created
- task completed
- completion recorded