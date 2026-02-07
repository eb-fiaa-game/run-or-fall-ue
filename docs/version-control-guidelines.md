# Version Control Guidelines

This project uses a simple solo workflow: a stable `main` branch and short-lived feature branches. All changes are merged back to `main` using squash merge, and commits follow strict Conventional Commits.

## Branching Strategy

- `main` is always stable and releasable.
- Work happens in short-lived branches and is merged back via squash.

## Branch Naming

Use one of the approved prefixes and a short slug in kebab-case (2 to 5 words).

**Format**
```
<prefix>/<slug>
```

**Prefixes**
- `feat/` new functionality
- `fix/` bug fixes
- `chore/` maintenance, tooling, refactors without behavior change
- `hotfix/` urgent production fixes

**Examples**
- `feat/player-jump-tuning`
- `fix/crash-on-respawn`
- `chore/update-asset-metadata`
- `hotfix/save-load-null`

## Commit Conventions (Strict Conventional Commits)

**Format**
```
<type>(<scope>): <subject>
```

**Rules**
- Use lowercase `type` and `scope`.
- `scope` is required and should be short (1-2 words).
- `subject` is imperative, lowercase, no trailing period.
- Keep the first line under 72 characters.

**Allowed types**
- `feat`, `fix`, `chore`, `docs`, `refactor`, `test`, `perf`, `build`, `ci`, `style`, `revert`

**Examples**
- `feat(movement): add coyote-time buffer`
- `fix(save): handle null slot names`
- `chore(build): update mac build scripts`
- `docs(readme): document branch naming`

## Merge Workflow (Solo, Squash Required)

1. Create a branch from `main` using the naming rules.
2. Commit work using strict Conventional Commits.
3. Rebase onto latest `main` if the branch is long-lived.
4. Squash merge into `main`.
5. The squash commit message must follow Conventional Commits.
6. Delete the branch after merge.

## Good Practices

- Commit in small, coherent slices with clear messages.
- Keep branches short-lived and focused on a single outcome.
- Avoid mixing asset changes with code changes when possible.
- If Git LFS is in use, keep large binary assets tracked by LFS.
- Tag releases when a playable milestone is reached.

