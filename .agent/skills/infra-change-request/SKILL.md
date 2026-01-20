---
name: infra-change-request
description: Mandatory protocol for executing system-level infrastructure changes.
role_required: true
tools:
  - run_command
  - gitea-issue-check
---

# Infrastructure Change Request Skill

## Prerequisites
*   **Strict Scope**: Applies to ALL system-level modifications (pkg install, firewall, service config).
*   **Trigger**: Usually follows a `system-triage` diagnosis.

## Workflow

### 1. Draft Change Request (CR)
*   **Action**: Create a CR Document (or Issue Description).
*   **Required Fields**:
    *   **Summary**: What is changing?
    *   **Reason**: Why?
    *   **Plan**: Step-by-step commands.
    *   **Rollback**: How to undo.
    *   **Verification**: How to test.

### 2. Approval
*   **Action**: Pause for User/Team Lead approval.
*   **Stop**: Do not proceed without explicit sign-off (`//ok-go`).

### 3. Execution (Real-Time Logging)
**CRITICAL**: Every command must be logged.

For EACH step in the Plan:
1.  **Announce**: Comment "Executing: <Description>".
2.  **Run**: Execute the command.
3.  **Log**: Post the exact command and full output to the Issue/Log.
    *   Format:
        ```markdown
        > Action Description
        > DO: `command`
        > OUT: `output`
        ```

### 4. Verification
*   **Action**: Run verification commands defined in Step 1.
*   **Log**: Post results.

### 5. Completion
*   **Action**: Close Issue or Mark Task Complete.
