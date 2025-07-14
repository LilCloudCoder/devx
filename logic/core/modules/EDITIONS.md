# Edition Modes – Internal Overview

This file documents the behavior, constraints, and responsibilities for each devx edition. These are not shown directly to the user, but guide how the system behaves based on selected mode.

## Core Principles (Applies to all)

- Each edition defines how much control the AI has.
- Editions decide which modules are activated.
- AI should never override or interfere with user intentions unless the edition explicitly allows guidance.
- No edition is allowed to access the internet or remote APIs. All models run locally.

## Edition Comparison Table

The following table outlines how each edition configures devx behavior. It helps internal agents determine which modules to load, how interactive the system should be, and how much freedom the AI has in modifying or guiding code.

| Feature               | Vibe     | Standard | Automate |
|-----------------------|----------|----------|----------|
| AI Generates Code     | ✅        | ❌        | ❌        |
| AI Edits Files        | ✅        | ❌        | ⚠️ (docs only) |
| Git Commands Enabled  | ⚠️ (only if guided) | ✅ | ✅ |
| Auto Commit / Push    | ❌        | ❌        | ✅ |
| CLI Only              | ✅        | ✅        | ✅ |
| Shell Access          | ✅        | ✅        | ✅ |
| Guidance Level        | High     | Low       | Minimal  |
| Docs Auto-Generated   | ✅        | ❌        | ✅ |
| Model Freedom         | Full     | Limited   | Restricted |

## Vibe Edition

This edition is designed for beginner developers or those who want a fully guided experience. The AI takes full responsibility for generating project structure, writing code, and asking interactive questions to guide the build. The user is expected to answer prompts rather than write code manually.

- AI has full creative freedom.
- Auto-generates files, folders, and logic.
- Best for full project bootstrapping.

---

## Standard Edition

This edition targets experienced developers who prefer manual control. The AI only provides suggestions, runs shell commands, and lints files. It does not create or modify code without direct input. Git actions are permitted but not automated.

- AI behaves like a passive shell assistant.
- Only works via direct CLI input.
- No code generation or editing.

---

## Automate Edition

This edition is for professional users who want automation *around* their code — not inside it. The AI handles commit generation, pushing, changelogs, and documentation without touching source code logic. It assumes the user writes and maintains code independently.

- AI is strictly restricted from editing code files.
- Git, doc, and cleanup tasks are fully automated.
- Useful for speeding up routine work.
