# Vendored Maven Artifacts

This directory is a project-local Maven repository used by `settings.gradle.kts`.

Vendored `io.github.libxposed` artifacts:

- `io.github.libxposed:api:100`
  - Source: `libxposed/api` commit `54582730315ba4a3d7cfaf9baf9d23c419e07006`
  - This artifact includes `io.github.libxposed.api.annotations.*`, which the current `core` sources require.
- `io.github.libxposed:interface:100`
  - Source: `libxposed/service` commit `e58452c` (`Add getRunningTargets API (#13)`), `interface` module.
  - This artifact matches the current daemon service implementation: API 100 naming, `HookedProcess`, `getRunningTargets()`, and single-argument `openRemoteFile(String)`.

Do not replace `api:100` with GitHub Packages `api-100-1.0.x` artifacts unless the classes are verified first; `api-100-1.0.2.aar` does not contain the annotation API required by this codebase.
