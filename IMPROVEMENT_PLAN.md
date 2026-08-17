# Completion plan

1. Treat repository hygiene as P0: a complete Windows-style `venv/` and PyCharm `.idea/` workspace are committed. These are generated/local artifacts and obscure whatever authored Python code exists.
2. Inventory authored `.py` files outside `venv/` and determine the actual exercises/tools represented before making any product or Python-engineering claims.
3. Add a Python-appropriate `.gitignore` covering virtual environments, caches, bytecode, IDE state and local environment files. Keep only intentionally shared IDE configuration, if any.
4. Remove the committed virtual environment from the cleanup branch after recording dependency/version information needed to reproduce it. Do not manually edit vendored `site-packages`.
5. Reconstruct dependencies from imports and/or existing metadata into a minimal pinned or bounded requirements/pyproject file. The committed pip 19/Python 3.8-era environment is not itself a maintainable dependency specification.
6. Audit code for hard-coded local paths, credentials, personal data and platform assumptions before making the repository public-facing.
7. Organize independent scripts/examples into clearly named directories or a small package only where that reflects actual relationships; avoid artificial architecture for learning snippets.
8. Add formatting/linting and focused tests only for authored logic worth maintaining. Do not test third-party packages copied inside the old virtualenv.
9. Verify a clean environment can install dependencies and run each documented script/example on a currently supported Python version, documenting legacy exceptions instead of silently rewriting behavior.
10. Rewrite README as a truthful Python learning/experiments archive: catalog of authored scripts, Python/dependency requirements, run commands, historical context and explicit exclusion of generated environment/vendor files from portfolio credit.
