# SOP: Git History Sanitization

**Status**: DRAFT
**Owner**: Rory Devlin (R&D)
**Version**: 1.0.0
**Last Updated**: 2026-01-20

## 1. Objective & Scope
This SOP provides a standardized protocol for identifying and removing prohibited language (offensive terms, sensitive data, etc.) from the Project's Git history and working tree. It governs all repositories under GNOMATIX control.

## 2. Prerequisites & Pre-flight Check
- **Tools**: `git`, `sed`, `grep`.
- **Reference**: [prohibited-terms.md](file:///home/brett/repos/icanhazslaves/private/docs/prohibited-terms.md) (Single Source of Truth).
- **Permissions**: Write access to the local and remote repository (Requires `force push` capability).
- **Environment**: Clean working directory (no unstaged changes).
- **Authorization**: Ad-hoc User authorization is REQUIRED before performing `git filter-branch` or `git push --force`.

## 3. Execution Protocol

### 3.1 Audit Phase
1. **Working Tree Search**:
   ```bash
   grep -rEi "term1|term2" .
   ```
2. **Commit Log Search**:
   ```bash
   git log --all --grep="term1" --grep="term2" -i
   ```

### 3.2 Mitigation Phase
1. **Working Tree Replacement**:
   Perform replacements in affected files using `sed` or IDE tools. Commit these changes before proceeding to history rewrite.
2. **History Rewrite**:
   Execute `git filter-branch` to scrub commit messages:
   ```bash
   FILTER_BRANCH_SQUELCH_WARNING=1 git filter-branch -f --msg-filter \
   'sed "s/term1/🤬/g; s/term2/🤬/g"' -- --all
   ```

### 3.3 Cleanup Phase
1. **Purge Backups**:
   ```bash
   rm -rf .git/refs/original/
   ```
2. **Prune Objects**:
   ```bash
   git reflog expire --expire=now --all && git gc --prune=now
   ```

## 4. Verification & Testing
- [ ] **Log Verification**: Run `git log` and search for prohibited terms to ensure replacement.
- [ ] **Hash Reachability**: Verify that the original offensive commit hashes are no longer reachable (e.g., `git log -1 <old-hash>` should fail).
- [ ] **Remote Integrity**: Verify remote state after push.

## 5. Rollback & Contingency Plan
1. **Local Reflog**: Use `git reflog` to identify the state prior to the filter-branch.
2. **Local Reset**: `git reset --hard <state-before-rewrite>`.
3. **Remote Restore**: If push was executed, restore from a verified clean backup or remote snapshot.

## 6. Audit Trail & Logging
- Record execution in `state/session/<GUID>/session_log_YYYY-MM-DD.md`.
- Reference specific commits and terms sanitized.

## 7. Sign-off
- **Author**: Rory Devlin
- **Reviewer**: Peter Milestone
- **Approval Date**: TBD
