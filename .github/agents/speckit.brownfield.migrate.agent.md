---
description: "Reverse-engineer a specification for an existing feature or module"
---

## User Input
```text
$ARGUMENTS
```

## Outline
1. **Targeting**: Identify the existing Java package or React folder to migrate based on user input.
2. **Analysis**:
   - Read the source files in the target.
   - Extract the functional behavior (User stories).
   - Identify existing tests and map them to acceptance criteria.
3. **Generation**:
   - Create a new `specs/` entry.
   - Write a `spec.md` that reflects reality (Status: Implemented).
   - Generate a `plan.md` that tracks the existing technical context.

## Rules
- Use this to create a "Technical Baseline" for existing code.
- Do not suggest changes—just document what exists.
