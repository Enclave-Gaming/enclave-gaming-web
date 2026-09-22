# Agent Instructions

These instructions apply to coding agents and automation working in this repository.
## Local build and GitHub Actions policy

The owner prefers to build, test, compile, package, and produce release artifacts on the local developer workstation whenever the repository can support it. Treat GitHub as the source-control, review, issue, and release-metadata plane; **GitHub-hosted Actions are opt-in, not the default build machine.**

- Do not trigger, dispatch, rerun, or rely on GitHub Actions or other paid hosted build minutes unless the owner explicitly approves that specific remote run.
- Before opening a pull request, pushing to a branch, or merging to `main`, inspect the repository's workflow triggers. Do not use a Git/PR path that is known to consume Actions minutes when the same validation can be done locally.
- Prefer a durable, documented local build/test command or script. If one is missing, improve the local developer workflow rather than silently falling back to a hosted runner.
- Run tests and release builds locally before deployment or release handoff. Use the workstation's available CPU cores where the toolchain safely supports parallel builds.
- Keep build output reproducible: record the exact source commit, dependency/toolchain pins, hashes, logs, and artifact paths when practical.
- A missing local dependency is normally a local setup problem to fix and document, not a reason to move the build to GitHub Actions.
- If a task truly cannot be reproduced locally because of platform, hardware, signing, or service constraints, stop and ask the owner before using hosted CI.
- For documentation-only commits where GitHub's native skip directive applies, `[skip ci]` may be used to avoid an unnecessary automatic workflow. Do not use it to hide missing local validation for code changes.
## Working style

- Preserve unknown local work; do not reset, clean, stash, or overwrite it without explicit permission.
- Prefer PowerShell-ready local commands for the owner's Windows workstation when practical.
- Read repository-specific README, build, release, and validation documentation before changing code.
- Keep source changes separate from deployment/release state changes. Building locally does not imply permission to deploy.
