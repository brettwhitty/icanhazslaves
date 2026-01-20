---
name: system-triage
description: Standardized diagnotic workflow for system and network issues.
role_required: true
tools:
  - run_command
  - send_command_input
---

# System Triage Skill

## Prerequisites
*   **Active Role**: Must be in a Role Context (e.g., `//office @it`).
*   **Issue Context**: Must be working on a specific issue (Jira/Gitea).

## Workflow

### 1. Acknowledge
*   **Action**: Comment on the issue acknowledging receipt.
*   **Message**: "Beginning investigation."

### 2. Define Problem
*   **Check**: Are timestamps, source IPs, and error messages present?
*   **Action**: If ambiguous, comment asking for clarification. STOP.

### 3. Live Investigation (Scout)
Execute sequentially. **Log every output**.

#### 3a. Network Socket Investigation
*   **Tool**: `ss`
*   **Command**: `ss -lupn | grep '<port>'`
*   **Goal**: Identify listening processes.

#### 3b. Process Investigation
*   **Tool**: `ps`
*   **Command**: `ps aux | grep -E -i '<keyword>'`
*   **Goal**: Identify running processes by name.

#### 3c. Service Status Check
*   **Tool**: `systemctl`
*   **Command**: `systemctl status <service>`
*   **Goal**: detailed status, config paths, logs.

### 4. Formulate Hypothesis
*   **Action**: Analyze data from Step 3.
*   **Output**: meaningful summary comment with evidence-based hypothesis.

### 5. Propose Action Plan
*   **Option A (Change Required)**: Propose specific system modification. Trigger `infra-change-request`.
*   **Option B (More Info)**: Outline specific next steps for deeper investigation.
