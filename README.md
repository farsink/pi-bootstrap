# Pi Bootstrap

Portable Pi package configuration for a fresh Linux or macOS installation.

## Includes

- The managed Pi package sources listed in `.pi/settings.json`
- Agent instructions for installing and verifying those packages

## Excludes

- Session history
- API keys, OAuth tokens, and `auth.json`
- Provider credentials and private endpoint keys
- Local extension and skill source code

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
5. Authenticate separately with `/login`, or provide the required API keys as environment variables.

Pi installs the package sources from `.pi/settings.json` and verifies them with `pi list`.

## Optional global installation

To make these packages available outside this repository, ask Pi:

```text
Install this repository's Pi packages globally.
```

Pi will install each manifest source into your user-level Pi configuration. Review `pi list` afterward.
