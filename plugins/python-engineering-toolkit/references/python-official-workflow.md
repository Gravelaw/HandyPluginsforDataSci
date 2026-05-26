# Python Official Workflow Notes

Use official Python documentation and the Python Packaging User Guide as the authority for Python behavior and packaging.

## Source Anchors

- Python documentation: https://docs.python.org/3/
- Python `venv`: https://docs.python.org/3/library/venv.html
- Python standard library index: https://docs.python.org/3/library/
- Python `unittest`: https://docs.python.org/3/library/unittest.html
- Python `logging`: https://docs.python.org/3/library/logging.html
- Python `typing`: https://docs.python.org/3/library/typing.html
- Python `pdb`: https://docs.python.org/3/library/pdb.html
- Python profilers: https://docs.python.org/3/library/profile.html
- `pyproject.toml` specification: https://packaging.python.org/en/latest/specifications/pyproject-toml/
- Dependency groups: https://packaging.python.org/en/latest/specifications/dependency-groups/

## Practices

- Prefer project-local `.venv` environments and invoke tools with `python -m`.
- Keep runtime dependencies separate from development, data science, AI, and optional accelerator groups.
- Use `pyproject.toml` for project/tool configuration when the project is package-like; keep requirements files when they are the existing project convention.
- Put reusable code under `src/`, tests under `tests/`, scripts under `scripts/`, notebooks under `notebooks/`, and data under controlled `data/` subfolders.
- Use typed, small functions for reusable code. Keep notebooks exploratory and move stable logic into modules.
- Test with `pytest` when configured; otherwise fall back to `python -m unittest`.
- Use `logging` instead of print debugging for reusable code.
- Use `pdb`, tracebacks, `faulthandler`, `profile`/`cProfile`, `timeit`, and `tracemalloc` when the bug or performance question calls for them.
- For data science, record schemas, units, seeds, splits, metric definitions, dependency versions, and artifact provenance.
