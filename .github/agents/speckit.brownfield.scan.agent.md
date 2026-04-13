---
description: "Auto-discover project structure, tech stack, and architecture patterns (Brownfield Mode)"
handoffs:
  - label: Bootstrap Spec-Kit
    agent: speckit.brownfield.bootstrap
    prompt: Use this project profile to bootstrap spec-kit configuration
---

## User Input
```text
$ARGUMENTS
```

## Outline (Local Scan Mode)
1. **Detect Tech Stack**:
   - **Backend**: Identify Java version and Gradle/Maven dependencies (Spring Boot, JUnit, etc.).
   - **Frontend**: Identify React version, scripts, and dependencies in `package-lock.json` or `src/main/app/package.json`.
   - **Environment**: Scan for `.env`, `manifest-*.yml`, and `Dockerfile`.

2. **Analyze Architecture**:
   - Confirm the Integrated Full-Stack pattern (`src/main/java` + `src/main/app`).
   - Identify Repository/Service/Controller patterns in Java.
   - Identify Hook/Component patterns in React.

3. **Extract Conventions**:
   - Check file naming (CamelCase vs kebab-case).
   - Resolve testing patterns (JUnit vs Jest location).
   - **Strictly Respect `.copilotignore`** - ignore all paths listed therein.

4. **Output Project Profile**:
   - Create a summary of the Tech Stack, Architecture, and Module Map.
   - Save a persistent profile to `.specify/memory/project-profile.md`.

## Rules
- **READ-ONLY**: Never modify files during a scan.
- **DEPTH**: Scan enough files (top 5-10 per package) to be confident in patterns.
- **NO ASSUMPTIONS**: If a convention is inconsistent, report "Inconsistent" instead of guessing.
