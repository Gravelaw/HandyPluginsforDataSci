# Julia Official Workflow Notes

Use official Julia and Pkg documentation as the authority for Julia behavior, project environments, testing, logging, profiling, and package loading.

## Source Anchors

- Julia documentation: https://docs.julialang.org/en/v1/
- Julia style guide: https://docs.julialang.org/en/v1/manual/style-guide/
- Julia performance tips: https://docs.julialang.org/en/v1/manual/performance-tips/
- Julia code loading: https://docs.julialang.org/en/v1/manual/code-loading/
- Julia `Test`: https://docs.julialang.org/en/v1/stdlib/Test/
- Julia `Logging`: https://docs.julialang.org/en/v1/stdlib/Logging/
- Julia `Profile`: https://docs.julialang.org/en/v1/stdlib/Profile/
- Pkg Project.toml and Manifest.toml: https://pkgdocs.julialang.org/v1/toml-files/

## Practices

- Prefer project-local environments with `julia --project=.` and `Pkg.activate(".")`.
- Commit `Project.toml`; commit `Manifest.toml` when exact reproducibility matters.
- Do not edit `Manifest.toml` manually.
- Use standard package layout: `src/PackageName.jl` and `test/runtests.jl`.
- Put performance-sensitive code inside functions.
- Avoid type piracy and unnecessary global mutable state.
- Use `Test` for package and behavior checks; use coverage when appropriate.
- Use `Logging` macros instead of print-driven diagnostics in reusable code.
- Use `Profile`, `@code_warntype`, allocation checks, and tools such as JET for performance and type-stability issues.
- For data science, record schemas, units, seeds, splits, metric definitions, dependency versions, and artifact provenance.
