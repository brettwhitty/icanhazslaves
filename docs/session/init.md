# Hello Session Initialization

This document defines the global handling of a **Hello** greeting, which serves as a session initiation trigger.

## Steps performed when a Hello is received
1. **Log the Greeting** – Append a line to the current session log (`state/session/<GUID>/session_log_YYYY-MM-DD.md`) noting the receipt of the greeting.
2. **Record Session State** – Record the session GUID and the path to the brain artifact (`./state/session/<GUID>/`) in the same log entry.
3. **Audit Gitea Backlog** – Add a placeholder entry indicating that the Gitea issue backlog was checked (e.g., "Backlog audit performed – no pending issues").
4. **Acknowledge** – Respond to the user with a concise confirmation that the greeting has been recorded and the session initialized.

These steps satisfy the requirements in `GEMINI.md` §13 (Session Initialization) and ensure a consistent, repeatable process for all sessions.
