# Python Repository Cleanup Plan

This repository currently preserves a local PyCharm / Python environment rather than a reproducible software project. The cleanup must prioritize recovery before deletion.

## 10 tasks

1. Inventory the committed `venv/` before removing anything and record interpreter/package metadata that may help identify the original project.
2. Search the environment and IDE metadata for references to missing project paths or entry points, without treating generated package code as authored application source.
3. Recover original `.py`, notebook, configuration or data files from backups/history if they still exist.
4. Create a dependency manifest (`requirements.txt` or `pyproject.toml`) only after the intended dependencies are identified.
5. Add a Python-focused `.gitignore` covering `.venv/`, `venv/`, `__pycache__/`, `.pytest_cache/`, local environment files and IDE state.
6. Remove the committed virtual environment from version control only after recovery is complete.
7. Remove or minimize `.idea/` project-local state unless specific shared IDE configuration is intentionally required.
8. Add a minimal source layout and tests only if original application source is recovered; do not fabricate a demo merely to make the repository look active.
9. Add reproducible setup/run/test commands after a real executable project exists.
10. Archive or make the repository private if no authored application source can be recovered; it should not be promoted as an engineering portfolio project in its current state.

## Portfolio decision

**Current recommendation: exclude from featured portfolio.**

A committed virtual environment demonstrates historical development activity but is weak evidence of authored software. The strongest action is repository hygiene and honest classification, not artificial feature expansion.

## Safety rule

Do not delete `venv/` or `.idea/` until recovery checks are complete. Historical metadata may be the only remaining clue to the original source.