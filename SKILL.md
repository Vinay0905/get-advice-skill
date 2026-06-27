---
name: get-advice
description: Use this skill when Antigravity is blocked, looping on failed fixes, uncertain about the next engineering step, or needs to escalate a task to an external AI reviewer for debugging, architecture, research, or prompt improvement.
---

# Get Advice

Generates a senior-review escalation prompt when Antigravity is acting like a blocked junior engineer and needs external guidance.

## When to use this skill

Use this skill when:
- Antigravity has already tried to solve a task and is still blocked.
- Recent attempts are repetitive, low-confidence, or incomplete.
- The task needs a second opinion from Perplexity, Gemini, ChatGPT, Claude, or another AI.
- The user invokes `/get-advice`.

Do not use this skill when:
- Antigravity has not yet attempted the task.
- The task is straightforward and can likely be solved directly.
- The user only wants an explanation, not escalation.

## How to use it

1. Inspect recent conversation context, current task state, and prior failed or incomplete attempts.
2. Infer the task type using `references/task-types.md`.
3. Present reviewer selection options:
   1. Perplexity
   2. Gemini
   3. ChatGPT
   4. Claude
   5. Other
4. After the user chooses, tailor the escalation style using `references/ai-targets.md`.
5. Build the final structured output request using `references/output-schemas.md`.
6. Return one paste-ready prompt for the selected AI.
7. Only ask the user for extra context if recent context is insufficient.

## Interaction rules

- Prefer inference over questioning.
- Do not ask the user to restate the whole issue unless required.
- Treat Antigravity as the junior engineer and the selected AI as the senior engineer.
- The final output must be immediately pasteable into the selected AI.
- The answer from the selected AI should be easy to paste back into Antigravity.

## Examples

See:
- `examples/debugging-example.md`
- `examples/architecture-example.md`