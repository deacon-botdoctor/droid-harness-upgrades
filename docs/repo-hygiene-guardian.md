# Repo hygiene guardian

A repo hygiene guardian reviews the workspace itself.

Check:

- branch and upstream status;
- dirty/staged/untracked files;
- stale worktrees;
- backup files;
- generated artifacts;
- broken tests/lint;
- docs drift;
- abandoned TODOs.

Before deleting anything, produce a cleanup manifest with target, reason, recovery path, and risk.
