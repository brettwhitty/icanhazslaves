# audit

## Description
The `audit` action type involves the systematic comparison of the current environmental state or proposed actions against established protocols, SOPs, or user directives.

## Scope
- Verifying if a state matches a described requirement.
- Checking for the existence of required directories or files before acting.
- Validating dependencies or tool availability.
- Assessing if a merged SOP is valid in the current repo context.

## Allowed Tools (Heuristic)
- Primarily a logical process utilizing `inspect` tools for data collection.
- `command_status`
- `list_resources`
- `read_resource`
