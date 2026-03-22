# shitty-clipboard-extension

Standalone clipboard extension for [pi coding agent](https://github.com/badlogic/pi-mono).

This package exposes one tool:

- `copy_to_clipboard`: copy arbitrary text to your local clipboard via OSC52.

## Install

```bash
pi install npm:shitty-clipboard-extension
```

Or for one session:

```bash
pi -e npm:shitty-clipboard-extension
```

## Usage

Ask the model:

- "Write me a draft reply and put it in my clipboard"
- "Generate a UUID and copy it to clipboard"

## How it works

The extension writes an OSC52 escape sequence to stdout. Most modern terminals support this, including iTerm2, Kitty, Alacritty, WezTerm, Windows Terminal, and tmux with clipboard passthrough enabled.

## Development (monorepo)

This package lives inside the `shitty-extensions` repository under:

- `packages/shitty-clipboard-extension`

## Publish

From repository root:

```bash
npm publish ./packages/shitty-clipboard-extension --access public
```
