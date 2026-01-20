# reflect

## Description
The `reflect` action type involves the agent communicating its current understanding of instructions, summarizing progress, and ensuring "Shared Truth" with the user.

## Scope
- Updating `task_boundary` TaskSummary and TaskStatus metadata.
- Generating responses that clarify instructions or confirm understanding.
- Notifying the user of state changes or requesting review.

## Allowed Tools (Heuristic)
- `task_boundary`
- `notify_user`
