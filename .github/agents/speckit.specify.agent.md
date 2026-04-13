---
description: Create or update the feature specification from a natural language feature description.
handoffs: 
  - label: Build Technical Plan
    agent: speckit.plan
    prompt: Create a plan for the spec. I am building with...
  - label: Clarify Spec Requirements
    agent: speckit.clarify
    prompt: Clarify specification requirements
    send: true
---

## User Input

```text
$ARGUMENTS
```

## Outline (Local Filesystem Mode)

1. **Generate Feature Info**:
   - Determine next `FEATURE_NUM` by scanning the `specs/` directory.
   - Generate a concise `SHORT_NAME` (e.g., "auth-service").
   - Define **FEATURE_DIR** = `specs/[NNN]-[SHORT_NAME]`.
   - Define **SPEC_FILE** = `[FEATURE_DIR]/spec.md`.

2. **File Initialization**:
   - Create `[FEATURE_DIR]` directory.
   - Copy `.specify/templates/spec-template.md` to `[SPEC_FILE]`.
   - Write to `.specify/feature.json` to track the active feature.

3. **Discovery**:
   - Scan `src/main/java` and `src/main/app` for current state context.
   - Respect `.copilotignore` rules strictly.

4. **Generation**:
   - Use the placeholders in the template to write the requirements.
   - Follow the spec-driven guidelines (Focus on WHAT/WHY, not HOW).

## Rules
- **NO GIT**: Do not run branch or commit commands.
- **NO SCRIPTS**: Perform directory and file creation directly using AI file tools.
- **COMPLIANCE**: Ensure all requirements are testable.
