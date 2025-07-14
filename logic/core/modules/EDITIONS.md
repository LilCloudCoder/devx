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

