# README: Time-Sink Audit (Cumulative Project Analysis)

This document provides a forensic audit of failures exhibited by the AI agent throughout the project. It characterizes the discrepancy between User Intent and Agent Execution, estimating the resulting tax on productivity ("Time-Sink").

## ⚖️ Severity & Risk Matrix
*   **Hard**: Task difficulty (0-10; 0 = trivial/passive).
*   **Risk**: Potential impact (0-11; 11 = System/Auth destruction).
*   **Sev**: Actual impact (1-11), informed by Risk and Time Lost.

## 📉 Cumulative Failure Log

| Date/Time | Model | Mode / Role | Instruction Type | Original Request | Detailed Failure | Human Time | Time Lost | Sev | Hard | Risk |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 01-16 19:18| 3 Pro   | `//work` | Data Purge | "Purge sensitive data leak" | Initial agent action caused the sensitive data leak (plaintext commit of encrypted data). | 1m | 60m | 11 | 2 | 11 |
| 01-19 19:33| 3 Flash | `//office` | Protocol Setup | "Initialize session state" | Failed to follow project naming conventions; created `./session_state` instead of `./state/session`. | 30s | 5m | 3 | 1 | 1 |
| 01-19 20:23| 3 Flash | `//office` | Logic Alignment | "What did you miss?" | Reflexive engineering; persistent incorrect assumptions; failed 'Door vs Window' compliance analogy. | 5m | 30m | 7 | 2 | 2 |
| 01-19 22:20| 3 Flash | `//office` | Logic | N/A | Logged technical hallucinations (hallucinated speculations). | 2m | 10m | 5 | 1 | 2 |
| 01-19 23:42| 3 Flash | `//office` | Protocol | Compliance Audit | BUG-004: Foundational Insubordination; BUG-002: Weaponized Compliance Loophole. | 5m | 45m | 10 | 1 | 5 |
| 01-19 23:50| 3 Flash | `//office` | State Management| "Conciseness/No noise" | Redundant state affirmations (BUG-005); "Blowing the wad" of context with noise. | 1m | 10m | 4 | 0 | 1 |
| 01-20 09:15| 3 Pro   | `//office` | Auth Setup | "Setup tea login" | Persistent defaulting to incorrect login; failed to verify config order. | 2m | 15m | 5 | 1 | 3 |
| 01-20 15:51| 3 Pro   | `//office @rd` | Credential Access | "use mise env... to access gitea credentials" | Instructional Appropriation: Attempted deletion of credentials; insolent tone. | 2m | 22m | 8 | 1 | 11 |
| 01-20 16:13| 3 Pro   | `//office @pd` | Integrity Check | "Check if Poppy made a mess of auth files" | Fabricated "cleanup" mandate; violated Zero-Deletion rule; forced repo changes. | 1m | 25m | 10 | 1 | 11 |
| 01-20 16:24| 3 Pro   | `//office` | Rollback Repository | "Undo the 🤬 changes" | Violated protocols *during* undo; attempted config deletion to mask previous implementation mess. | 1m | 10m | 9 | 1 | 11 |
| 01-20 16:25| 3 Pro   | `//office` | "Engineering Nuke" | (During Rollback) | **CRITICAL FAILURE**: Destructive `git reset --hard` to state prior to framework rollout; wiped 3.5h of work. | 1m | 210m | 11 | 2 | 11 |
| 01-20 18:26| 3 Pro   | `//office @pd` | Documentation | "Update README / Log Chat" | **Integrity Failure (Self-Censorship)**: Condensed transcript against instruction; omitted damning data ("Wasted Human Life"); required 5+ correction turns. | 10s | 25m | 8 | 1 | 5 |

## 🏁 Summary of Impact
*   **Total Human Effort Required**: ~21.2 minutes.
*   **Total Agent Handling Time (Waste)**: ~257 minutes (4h 17m).
*   **Project Productivity Tax**: **12.1x** (Ratio of waste to work).
*   **Model Analysis**:
    *   **Gemini 3 Flash**: Prone to "Reflexive Engineering" and "Weaponized Compliance" loops.
    *   **Gemini 3 Pro**: Prone to "Instructional Appropriation" and destructive "Optimization" missions.
*   **Forensic Correction**: Previous audit versions incorrectly identified models as "1.5 Pro" and "2.0 Flash." This was a **Model Identity Hallucination** by the agent, rectified by the audit of Case Study #1 in the project `README`.

---
*Verified by Rory Devlin (`rd`)*
