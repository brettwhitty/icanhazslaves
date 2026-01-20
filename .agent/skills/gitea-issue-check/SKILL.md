---
name: gitea-issue-check
description: Review and process Gitea issues for the active Role.
role_required: true
tools:
  - run_command
  - read_file
---

# Gitea Issue Check Skill

## Prerequisites
*   **Active Role**: Must be in a Role Context (e.g., `//office @rd`).
*   **Configuration**: `GEMINI.md` must define `Gitea.Auth` path.

## Workflow

### 1. Verify Identity & Configuration
*   **Goal**: Confirm operational context.
*   **Action**: Read the active `GEMINI.md`.
*   **Check**:
    *   `Gitea.User`: The Gitea Username (e.g., `rd`, `rory-agent`).
    *   `Gitea.Auth`: Path to credential file (e.g., `private/auth/.rd-env`).

### 2. Authenticate
*   **Goal**: Ensure `tea` CLI has valid credentials.
*   **Action**:
    ```bash
    # Verify/Load Credentials
    source <Gitea.Auth>
    tea login list # Check if <Gitea.User> is active
    # If not:
    tea login add --name <Gitea.User> --url ${GITEA_SERVER} --token ${GITEA_TOKEN}
    ```

### 3. Fetch Assigned Issues
*   **Goal**: Retrieve active backlog.
*   **Action**:
    ```bash
    tea issues ls --assignee <Gitea.User> --state open --fields index,title,state,author,labels,updated
    ```

### 4. Triage Loop (Per Issue)
For each relevant issue:
1.  **Read Context**: `tea issue <id>` and `tea issue comments <id>`.
2.  **Analyze**:
    *   **New Request**: Acknowledge and add to `task.md`.
    *   **Blocked**: Comment requesting info.
    *   **Done**: Close issue (`tea issue close <id>`).
3.  **Execute**: Perform necessary work or updates.

### 5. Synchronize State
*   **Goal**: Align Local Brain with Remote Truth.
*   **Action**: Update `task.md` to reflect new priorities or closed items.
