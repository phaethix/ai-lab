# AGENTS.md

This file is the collaboration contract for this repository. It applies to AI coding agents and human developers alike.
Rules are numbered: append new rules under the next free number, and never renumber or reuse an existing one.

## Project Overview

- Purpose: a hands-on workspace for studying large language model internals
- Stack: Python ≥ 3.13, uv (package management and execution), PyTorch, Transformers
- Layout:
  - `src/ai_lab/` — reusable library code
  - `notebooks/` — exploratory notebooks (inference walkthroughs, architecture comparisons, math foundations)

## Mandatory Rules

### R1 — Code Formatting

**Rule**: after writing or modifying any code, run:

```bash
uvx ruff format --no-cache .
```

**Why**

- Enforces one style and removes formatting noise from diffs, so reviews focus on logic
- `--no-cache` keeps `.ruff_cache/` out of the repository root

**Scope**

- All Python sources (`src/`) and notebooks (`notebooks/*.ipynb`)
- Applies to every change, including single-line edits

**When**

- As the final action before committing
- If formatting rewrites files, re-check the result before committing

## Common Commands

```bash
uv sync                            # install dependencies
uv run jupyter lab                 # start Jupyter
uv run python -c "import ai_lab"   # verify the package imports
```

## Reserved Rules

The following numbers are reserved and will be filled in as the project evolves:

- R2 — (TBD)
- R3 — (TBD)

## Maintenance

- **Add a rule**: take the next unused number and append it to Mandatory Rules
- **Change a rule**: edit the body but keep the number, so external references stay valid
- **Retire a rule**: mark it `(deprecated)` and point to its replacement; do not delete it
