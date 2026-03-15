# Internal Request Tracking Automation

A sanitized case study of an internal request automation workflow built to improve request intake, execution tracking, and completion visibility.

> Note: this repository is intentionally anonymized and simplified due to NDA restrictions. It focuses on workflow design, process logic, and engineering decisions rather than proprietary implementation details.

## Overview

This project represents a low-code automation workflow for handling internal requests from submission to completion tracking.

The solution was designed to:
- reduce manual request handling
- improve status visibility
- create a reliable execution trail
- support lightweight operational reporting

## Problem

Internal requests were collected manually and required extra follow-up to track execution status and completion. This created gaps in visibility, increased manual coordination, and made it harder to maintain a reliable execution log.

## Solution

The workflow starts with a request submitted through a form. The request is recorded in a spreadsheet and pushed into a task board for execution. A separate completion workflow listens for task completion events and writes structured completion data into a reporting sheet.

This design provided a complete request lifecycle view:
- request submitted
- task created
- task completed
- completion logged with date and responsible person

## Architecture

Form Submission  
→ Spreadsheet (request intake log)  
→ Automation Workflow 1  
→ Task Board  

Task Completed  
→ Automation Workflow 2  
→ Completion Log Sheet / Reporting Layer

More details: see [`docs/architecture.md`](docs/architecture.md)

## My role

I designed and implemented the workflow logic, including:
- intake and completion flow design
- low-code automation setup
- task board integration
- completion tracking logic
- reporting-oriented spreadsheet structure
- practical adaptation to platform constraints

## Key engineering decisions

### Multi-workflow design
Due to limitations in the available automation tier, the process was split into separate intake and completion workflows. This kept the automation reliable and easier to operate while still covering the full request lifecycle.

### Reporting-oriented completion log
Instead of relying only on the active task board state, the solution writes completion records into a reporting sheet that preserves date and executor information.

### Low-friction adoption
The workflow was built around simple tools already familiar to users, which helped adoption and ongoing use.

## Example stack

- Google Forms
- Google Sheets
- Zapier
- Trello

## Example outcomes

- unified request intake flow
- clearer execution visibility
- reduced manual follow-up
- structured completion history
- practical internal reporting

## Portfolio note

This repository is a sanitized case study created to demonstrate:
- low-code workflow design
- internal tool automation
- process-oriented thinking
- handling platform constraints pragmatically
- building useful systems with lightweight tools
