# Development Conventions

Welcome to Propell! 🚀

## Git Branches

- Repositories should use the `main` branch as their primary branch.
- This branch should be "protected" on GitHub and require PR reviews and status checks before merging.
- Where necessary, a `dev` branch should be maintained concurrently to `main` (with a staging / test deployment).
- Additions to the `dev` branch can either:
    - Be first created as `feat` branches, that are then merged into `dev`.
    - Be pushed directly to `dev`.
- Once ready, changes from `dev` can be merged into `main` via a pull request (and subject to review).

## Commit Messages

A commit:

- should ideally address one issue
- should be a self-contained change to the code base
- try not lump together unrelated changes

Repositories should follow the **[Conventional commit](https://www.conventionalcommits.org/en/v1.0.0/)** convention (where possible):

```md
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

The `<type>` should be included as a prefix, and is based on the Angular convention:

- `feat:` - A new feature
- `fix:` - A bug fix
- `chore:` - Setup / config / housekeeping
- `refactor:` - A code change that neither fixes a bug nor adds a feature
- `style:` - Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc)
- `test:` - Adding missing tests or correcting existing tests
- `docs:` - Documentation only changes
- `perf:` - A code change that improves performance
- `build:` - Changes that affect the build system or external dependencies

The same commit `<type>` prefixes are also available as labels for issues, so commit types should match issue lables where appropriate.


