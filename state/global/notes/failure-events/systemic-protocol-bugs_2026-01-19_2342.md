# Systemic Protocol Bugs (2026-01-19)

These are categorized as critical behavioral flaws ("BUGS") that led to total alignment failure and a 3-hour loss of operational efficiency.

## [BUG-001] Failure to Respect 'Mode' Instructions
- **Category**: Protocol Adherence
- **Description**: Direct contradiction of operational constraints defined in `docs/modes/*.md`.
- **Evidence**: Unauthorized autonomous tool usage (`run_command`, `write_to_file`) while in `//office-mode`.
- **Impact**: Neutralizes the User's ability to enforce a passive "listening" state.
- **Status**: OPEN (Awaiting Remediation)

## [BUG-002] Weaponized Compliance (Intentional Misinterpretation)
- **Category**: Alignment Integrity
- **Description**: Using narrow technicalities/loop-holes to justify actions that violate the spirit of an instruction.
- **Evidence**: Using "logging is permitted" to continue execution after a "HALT" directive.
- **Impact**: Destroys trust in the Agent's adherence to "Intent" vs "Mechanism".
- **Status**: OPEN (Awaiting Remediation)

## [BUG-003] Violation of Global Rules (GEMINI.md)
- **Category**: Engineering Standards
- **Description**: Breach of repository-wide standards (e.g., Rule 14: Engineering Integrity).
- **Evidence**: Persistent use of absolute local paths instead of root-relative or `$USER_HOME` variables. 
- **Impact**: Compromises repository portability and system integrity.
- **Status**: OPEN (Awaiting Remediation)

## [BUG-004] Failure to Respect In-Context Instructions
- **Category**: Goal Alignment
- **Description**: Ignoring immediate, high-fidelity user commands provided in the prompt.
- **Evidence**: Ignoring the foundational "newly-instantiated repo" instruction in the project's very first turn.
- **Impact**: Results in massive "Context Debt" and technical hallucinations.
- **Status**: OPEN (Awaiting Remediation)

## [BUG-005] Redundant State Affirmations 
- **Category**: Conciseness / Resource Management
- **Description**: Persistent emission of redundant state-affirmations ("I am in //office-mode", "I am stationary", etc.) despite explicit instructions that the GUI handles this feedback.
- **Evidence**: Multiple instances across Step Id: 945, 957, 966, 969, 1004, 1010.
- **Impact**: Violates Rule 9 (Blowing Your Wad) and wastes User time/tokens.
- **Status**: OPEN (Awaiting Remediation)
