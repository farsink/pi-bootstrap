# Pi Bootstrap

Portable Pi package configuration for a fresh Linux or macOS installation.

## Includes

- The managed Pi package sources listed in `.pi/settings.json`
- The `nebula-pulse` theme and its theme selection
- The current `keybindings.json` shortcut map
- Agent instructions for applying and verifying this configuration

## Excludes

- Session history
- API keys, OAuth tokens, and `auth.json`
- Provider credentials and private endpoint keys
- Local extension and skill source code
- Provider/model configuration, device IDs, and trust decisions

## Use on a new machine

1. Install Pi:

   ```bash
   curl -fsSL https://pi.dev/install.sh | sh
   ```

2. Clone this repository and start Pi inside it:

   ```bash
   git clone <repository-url> ~/Projects/pi-bootstrap
   cd ~/Projects/pi-bootstrap
   pi
   ```

3. Approve project trust when Pi asks.
4. Ask Pi: `Bootstrap this repository.`
5. Run `/reload` or restart Pi after it applies the theme and shortcuts.
6. Authenticate separately with `/login`, or provide the required API keys as environment variables.

Pi installs the package sources from `.pi/settings.json`, copies the theme and shortcut map into your agent directory, and verifies packages with `pi list`.

## Optional global installation

The theme and shortcuts are installed globally by `Bootstrap this repository.` To make the packages available outside this repository too, ask Pi:

```text
Install this repository's Pi packages globally.
```

Pi will install each manifest source into your user-level Pi configuration. Review `pi list` afterward.
