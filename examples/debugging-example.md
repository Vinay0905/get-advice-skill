# Debugging Example

Scenario:
Antigravity attempted to fix a React build error multiple times but the project still fails to compile.

Expected behavior:
- Infer task type as debugging.
- Show reviewer options.
- After reviewer selection, generate a prompt that includes:
  - objective,
  - blocker,
  - attempted fixes,
  - constraints,
  - debugging-oriented output requirements.