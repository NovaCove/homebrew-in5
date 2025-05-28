# Homebrew Tap for NovaCove Tools (in5)

This is a [Homebrew](https://brew.sh) tap for NovaCove tools. It currently includes:

- [Imbued](https://github.com/novacove/imbued): A toolset for managing secrets in a development environment

## Installation

```bash
# Add the tap
brew tap novacove/in5

# Install imbued
brew install imbued
```

## Usage

After installation, follow the instructions in the caveats to set up shell integration.

### Bash

Add to your `.bashrc` or `.bash_profile`:

```bash
export IMBUED_BIN=$(brew --prefix)/bin/imbued
source $(brew --prefix)/share/imbued/scripts/bash/imbued.sh
```

### Zsh

Add to your `.zshrc`:

```zsh
export IMBUED_BIN=$(brew --prefix)/bin/imbued
source $(brew --prefix)/share/imbued/scripts/zsh/imbued.zsh
```

### Fish

Add to your `config.fish`:

```fish
set -gx IMBUED_BIN (brew --prefix)/bin/imbued
source (brew --prefix)/share/imbued/scripts/fish/imbued.fish
```

## Server Mode

To run Imbued in server mode, you can install it as a launchd service:

```bash
brew services start imbued
```

When using server mode, also set the socket path in your shell configuration:

```bash
# For Bash/Zsh
export IMBUED_SOCKET=$HOME/.imbued/imbued.sock

# For Fish
set -gx IMBUED_SOCKET $HOME/.imbued/imbued.sock
```

## License

MIT
