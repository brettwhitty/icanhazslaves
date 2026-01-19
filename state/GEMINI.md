# Agent State Management (state/)

This directory manages the persistence of agent state across sessions, bridging the gap between the stateless LLM and the project lifecycle.

## Hierarchy Structure

### 1. `state/session/<SESSION_GUID>/` (LOCAL / IGNORED)
- **Purpose**: The "Sandbox" / "Working Buffer."
- **Contents**: Session-specific logs, ephemeral task mirrors, and high-verbosity debugging data.
- **Persistence**: Local to the developer's machine and specific to the IDE session.
- **Git Status**: IGNORED. Never commit this directory.
- **Link**: Deterministically linked to the IDE's internal brain directory via the `<SESSION_GUID>`.

### 2. `state/global/` (TRACKED / PERSISTENT)
- **Purpose**: The "Gold Standard" / "Project Memory."
- **Contents**: Verified patterns, cross-session architectural decisions, and promoted outcomes.
- **Persistence**: Shared across the project and team.
- **Git Status**: TRACKED. Changes should be reviewed and committed.

## Protocol for the Agent

1. **Verification**: ALWAYS check for the existence of `state/` and the current `state/session/<SESSION_GUID>/` before beginning work.
2. **Promotion**: If a pattern or decision discovered during a session is deemed high-fidelity, it should be promoted from `session/` to `global/`.
3. **Forensic Integrity**: Maintain the `session_log.md` within the GUID directory to ensure deep auditing capability.
