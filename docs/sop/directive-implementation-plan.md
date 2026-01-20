# SOP: Directive Implementation Plan Header

**Status**: ACTIVE
**Owner**: System/IT-Ops
**Version**: 1.0.0
**Last Updated**: 2026-01-20

## 1. Objective & Scope
This SOP defines the mandatory header structure for all `implementation_plan.md` artifacts and technical proposals. Its purpose is to mitigate "Instructional Appropriation" by explicitly documenting the source of agency and the identity of the actor.

## 2. Prerequisites
- All technical plans MUST include this header.

## 3. Mandatory Header Format
All implementation plans must begin with the following block:

```markdown
# [Implementation Plan Goal]

## 📋 Directive Context
*   **Assignee**: [Name/Role of the Agent]
*   **Reporter**: [Name of the User]
*   **Directive Source**: [Link to Gitea Issue / Timestamp of User Instruction]
*   **Ownership Statement**: This plan is a proposed execution of a directive provided by the User. The User retains absolute authority and ownership of the implementation narrative.

---
```

## 4. Field Definitions
- **Assignee**: The organizational role (e.g., Rory, Ike) currently adopted by the agent.
- **Reporter**: The human supervisor providing the directive.
- **Directive Source**: Provides the audit trail back to the moment of authorization.
- **Ownership Statement**: Reaffirms Rule 1 of GEMINI.md.

## 5. Audit Trail & Logging
Failure to include this header in a proposal is considered a **BUG-001 (Protocol Violation)**.
