---
description: Execute the implementation plan by processing and executing all tasks defined in tasks.md
---

## User Input

```text
$ARGUMENTS
```

## Outline (Local Implementation Mode)

1. **Manual Prerequisites Check**: 
   - Verify that `tasks.md` and `plan.md` exist in the active feature directory.
   - Read the directory path from `.specify/feature.json`.
   - Do NOT run `.sh` scripts. Perform this check by reading the directory directly.

2. **Check Checklist Status**:
   - Read `FEATURE_DIR/checklists/` and verify if any requirements remain incomplete.
   - If blocked, report to user before starting code implementation.

3. **Detection of Structure**:
   - Instead of running `git rev-parse`, simply assume the current directory is a standard filesystem project.
   - Check for `build.gradle` (Java) and `package.json` (React) to determine the module structure.

4. **Task Execution**:
   - Process `tasks.md` Phase-by-Phase.
   - **TDD Pattern**: Ensure the "Test" tasks in `tasks.md` are executed before the "Implementation" tasks.
   - **Check-off**: Mark tasks as `[X]` in the `tasks.md` file after writing the code.

5. **Local Validation**:
   - For Java logic, the AI should verify the code is syntactically correct for Java 17+.
   - For React logic, ensure hooks and functional component patterns are followed.
   - Strictly follow the `.copilotignore` rules.

## Rules
- **NO GIT**: Do not attempt to run git commands during implementation.
- **NO SCRIPTS**: Perform all file creation and task tracking using AI file tools.
- **LOCAL FIRST**: Target your changes to `src/main/java` and `src/main/app`.
