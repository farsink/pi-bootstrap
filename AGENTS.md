# Agent Instructions

## Package Manager
Use Pi package commands:

```bash
pi update --extensions
pi list
pi install <package-source>
```

## Bootstrap
- When asked to bootstrap this repository, run `pi update --extensions`, then `pi list`.
- Treat `.pi/settings.json` as the canonical managed-package manifest.
- When explicitly asked to install globally, install every source in `.pi/settings.json` with `pi install <package-source>`.
- Do not copy session files, `auth.json`, API keys, OAuth tokens, provider credentials, or extension source code.
- Use `/login` or environment variables for credentials.

## Key Conventions
- Keep this repository portable: package names and non-secret setup documentation only.
- Add or remove managed extensions only through `.pi/settings.json`.
- Verify package changes with `pi list`.

## Commit Attribution
AI commits MUST include:

```
Co-Authored-By: <agent model name> <noreply@example.com>
```
