# get-advice — Antigravity Global Skill

A custom Agent Skill for Google Antigravity that escalates blocked tasks to an external AI reviewer.

## What it does

When Antigravity gets stuck, this skill acts like a junior developer escalating to a senior developer.
It inspects recent context, infers the task type, presents AI reviewer options, and generates a
paste-ready structured prompt you can send to Perplexity, Gemini, ChatGPT, Claude, or any other AI.

## How to install (global)

1. Ensure your skill is in the correct path:
   ~/.gemini/config/skills/get-advice/

2. If you installed it elsewhere, create a symlink:
   ln -s ~/.gemini/antigravity/skills/get-advice ~/.gemini/config/skills/get-advice

3. Restart Antigravity or start a new conversation.

4. Invoke with: /get-advice

## Common gotcha (path issue)

Antigravity's global skill loader scans ~/.gemini/config/skills/, NOT ~/.gemini/antigravity/skills/.
If your skill isn't being discovered, this is likely why.

## Usage

Type /get-advice or say "Run get-advice" in any Antigravity conversation.

1. Skill inspects recent context and infers the task type.
2. Presents reviewer options (Perplexity, Gemini, ChatGPT, Claude, Other).
3. Generates a paste-ready escalation prompt tailored to your chosen AI.
4. Paste the result into that AI, paste its answer back into Antigravity.

## Folder structure

```text
get-advice/
├── SKILL.md
├── references/
│   ├── task-types.md
│   ├── ai-targets.md
│   └── output-schemas.md
└── examples/
    ├── debugging-example.md
    └── architecture-example.md
```
