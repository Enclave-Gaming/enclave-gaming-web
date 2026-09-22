# Repository instructions for GitHub Copilot and coding agents

Read and follow `AGENTS.md` before making changes.

The owner's build policy is **local-first**. Build, test, compile, package, and create release artifacts on the developer workstation whenever possible. GitHub Actions and hosted runner minutes are opt-in only; do not trigger, dispatch, rerun, or cause them through PR/push/merge workflows without explicit approval for that run.

Prefer reproducible local scripts and PowerShell-ready commands. A missing local dependency should normally be installed and documented locally rather than using hosted CI as a fallback.
