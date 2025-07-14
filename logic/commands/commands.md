# devx Commands Reference

This file documents all available CLI commands used within the `devx` developer automation tool. Each command is modular, silent by default, and intended for use in professional or semi-automated coding workflows.

---

## 🔧 `devx config`

Configure your system edition, assign models, and manage preferences.

### Usage:
> devx config --edition "automate"  
> devx config models "llama3" --git "gemma" --docs "qwen3"

### Flags:
- `--edition <name>` → Sets system mode (internal behavior switch)
- `models <core>` → Assigns base model
- `--git`, `--docs`, etc. → Assigns role-specific models

---

## 🚀 `devx run`

Executes the core behavior based on the current edition. This is the main command users interact with.

### Usage:
> devx run

### Behavior:
- Loads shell, model, and config logic
- Executes edition-specific flows
- Triggers file edits, commits, doc gen (based on mode)

---

## 🛠️ `devx edit`

Allows manual editing of a file with AI suggestions or diffs.

### Usage:
> devx edit path/to/file.py

### Flags:
- `--explain` → Print suggested change with explanation
- `--apply` → Auto-apply suggestions (Vibe only)

---

## 🌱 `devx init` *(optional)*

Initializes a new project structure with base folders and optional git init.

### Usage:
> devx init my-project

---

## 📤 `devx push`

Pushes recent commits to GitHub. Available in `standard` and `automate` modes.

### Usage:
> devx push

---

## 🧠 `devx docs`

Generates or updates `README.md`, changelogs, or markdown docs based on existing code and commit history.

### Usage:
> devx docs

---

## ⚙️ Internal Commands

These are internal and usually triggered during `run`.

- `main.py` → Dispatch point
- `shell.py` → Runs shell safely
- `git.py` → Handles `stage`, `commit`, `push`
- `docx.py` → Handles docs generation

---

*Note: All commands respect the current edition rules and will disable or restrict behavior based on internal logic.*