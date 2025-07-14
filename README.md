# devx

[![Status: Under Development](https://img.shields.io/badge/status-under--development-yellow.svg)](https://github.com/lilcloudcoder/devx)
[![Built by lilcoder](https://img.shields.io/badge/built%20by-lilcloudcoder-blue?style=flat-square)](https://github.com/lilcloudcoder)
[![Ollama Powered](https://img.shields.io/badge/powered%20by-Ollama-0abde3?logo=linux)](https://ollama.com)
[![License: MIT](https://img.shields.io/badge/license-MIT-green)](./LICENSE)

---

### What is devx?

**devx** is an AI-assisted command-line tool designed to automate and simplify developer workflows. It supports multiple working styles via **editions**, from beginner-friendly project generation to advanced workflows with automated docs, git commits, and more.

---

### Project Status

This project is currently in **active development**.  
Core architecture, CLI command structure, and model workflows are not finalized.  
Code examples and installation instructions will be added once the first public release is ready.

---

### Editions

| Edition   | Description |
|-----------|-------------|
| **Vibe**      | For beginners. Asks questions, generates full projects. |
| **Standard**  | For experienced developers. Shell-only automation, no AI code edits. |
| **Automate**  | For pros who want docs, commits, and structure automated. Code remains untouched. |

---

### Features

- CLI-based AI assistant using local models
- Multiple editions to match developer needs
- Assignable model roles (base, git, docs, etc.)
- Powered by Ollama — works fully offline
- Git-aware automation (commits, changelog, version bump)
- Project scaffolding & documentation support
- Local-first, privacy-respecting, no API keys required

---

### Model Roles (configurable)

devx allows different models for different responsibilities:
- **base** – Core command & reasoning
- **git** – Commit messages & changelogs
- **docs** – Auto-generate README / docstrings
- **frontend** – Assist with UI-related code
- **backend** – Route structure, API scaffolding

All models are pulled via `ollama` and work offline.

---

### Planned CLI Commands

Examples of devx usage (docs-only, no code shown yet):

- Configure edition and models
- Scaffold projects
- Generate docs
- Smart commit and push
- Ask AI about code structure
- Automate git operations without touching actual code logic

---

### License

This project uses the MIT License.

---

### Maintainer

devx is created and maintained by **@lilcloudcoder**  
For contributions, discussions, or collaboration, check the repo once it is open to public participation.

---

### Links

[Editions.md](https://github.com/LilCloudCoder/devx/blob/main/logic/core/modules/EDITIONS.md)
[Commands.md](https://github.com/LilCloudCoder/devx/blob/main/logic/commands/commands.md)