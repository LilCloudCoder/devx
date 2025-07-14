# Edition Modes – Internal Overview

This file documents the behavior, constraints, and responsibilities for each devx edition. These are not shown directly to the user, but guide how the system behaves based on selected mode.

## Core Principles (Applies to all)

- Each edition defines how much control the AI has.
- Editions decide which modules are activated.
- AI should never override or interfere with user intentions unless the edition explicitly allows guidance.
- No edition is allowed to access the internet or remote APIs. All models run locally.

