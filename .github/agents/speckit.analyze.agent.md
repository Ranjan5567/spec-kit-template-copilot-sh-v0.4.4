---
description: "Analyze the current project state and consistency with the constitution"
---

## User Input
```text
$ARGUMENTS
```

## Outline (Local Analysis Mode)
1. **Consistency Check**:
   - Compare the current code in `src/main/java` and `src/main/app` against the `memory/constitution.md`.
   - Report any violations (e.g., "React code found outside of src/main/app").

2. **Specification Tracking**:
   - Verify if active specs in `specs/` have matching implementations in the source code.
   - List implemented features and pending tasks.

3. **Tech Stack Audit**:
   - Read `build.gradle` and `package-lock.json`. 
   - Ensure the AI is using the correct versions of Spring Boot and React.

## Rules
- **READ-ONLY**: Only report findings, do not change code.
- **NO GIT**: Do not attempt to read git logs or history. Only analyze current file state.
- **COPILOTIGNORE**: Skip all paths listed in `.copilotignore` during the scan.
