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
- Treat `.pi/settings.json` as the canonical managed-package manifest and theme selection.
- Copy `.pi/themes/nebula-pulse.json` to `<agent-dir>/themes/nebula-pulse.json`.
- Back up an existing `<agent-dir>/keybindings.json`, then replace it with this repository's `keybindings.json`.
- Merge `"theme": "nebula-pulse"` into `<agent-dir>/settings.json` without replacing unrelated settings.
- Ask the user to run `/reload` or restart Pi after copying UI configuration.
- When explicitly asked to install packages globally, install every source in `.pi/settings.json` with `pi install <package-source>`.
- Do not copy session files, `auth.json`, API keys, OAuth tokens, provider credentials, or extension source code.
- Use `/login` or environment variables for credentials.

## Key Conventions
- Keep this repository portable: package names, theme data, shortcuts, and non-secret setup documentation only.
- Add or remove managed extensions only through `.pi/settings.json`.
- Verify package changes with `pi list`.

## Commit Attribution
AI commits MUST include:

```
Co-Authored-By: <agent model name> <noreply@example.com>
```
