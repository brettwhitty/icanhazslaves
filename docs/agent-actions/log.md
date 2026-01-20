# log

## Description
The `log` action type involves updating persistent records of the agent's work, state, and session history to ensure accountability and auditability.

## Scope
- Appending entries to the current `session_log_YYYY-MM-DD.md`.
- Updating the internal `task.md` artifact to track progress and gates.
- Modifying the `user-directed-todo.md` tracker to reflect task state as instructed.

## Allowed Tools (Heuristic)
- `write_to_file` (targeting log/task/todo files)
- `replace_file_content` (targeting log/task/todo files)
- `multi_replace_file_content` (targeting log/task/todo files)
