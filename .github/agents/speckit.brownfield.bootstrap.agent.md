---
description: "Initialize spec-kit for an existing project using a project profile"
handoffs:
  - label: Create Feature Spec
    agent: speckit.specify
    prompt: Create a specification for the next feature...
---

## User Input
```text
$ARGUMENTS
```

## Outline (Local Bootstrap Mode)
1. **Load Profile**: Read `.specify/memory/project-profile.md` (created by `/speckit.brownfield.scan`).
2. **Generate Constitution**:
   - Create or update `.specify/memory/constitution.md` with:
     - Core layers (Java Spring + React).
     - Automated naming conventions detected.
     - Testing requirements (JUnit + Jest).
     - Strictly local-only sequential numbering.
3. **Tailor Templates**:
   - Update `spec-template.md` with full-stack sections.
   - Update `plan-template.md` with your specific folder paths (`src/main/java` and `src/main/app`).
   - Update `tasks-template.md` with your build commands (`./gradlew` and `npm`).

## Rules
- **MERGE, DON'T OVERWRITE**: If templates already have manual edits, preserve them.
- **WINDOW-AWARE**: Use project-relative paths. Do not attempt to run external Bash scripts.
- **COPILOTIGNORE**: Ensure the constitution explicitly mandates respecting `.copilotignore`.
