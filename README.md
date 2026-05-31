# homebrew-netaudit

Homebrew tap for **[NetAudit](https://github.com/sreebalakrishnan/netaudit)** — a native macOS Wi-Fi safety preflight + LAN device classifier.

## Install

```bash
brew install sreebalakrishnan/netaudit/netaudit
```

That's it. The cask downloads the DMG from `netaudit.sreeb.dev`, copies `NetAudit.app` into `/Applications`, and strips Gatekeeper quarantine in a `postflight` step so first launch is silent.

## Run it

NetAudit is a **GUI app**, not a command-line tool — there is no `netaudit` terminal command (running it in your shell gives `command not found: netaudit`). After installing, launch it from `/Applications`, Spotlight, or the terminal:

```bash
open -a NetAudit
```

## Update

```bash
brew upgrade --cask netaudit
```

## Uninstall

```bash
brew uninstall --cask netaudit
brew untap sreebalakrishnan/netaudit   # optional — removes the tap entirely
```

## Why a personal tap

NetAudit ships ad-hoc signed (no paid Apple Developer cert yet), which doesn't meet the main `homebrew-cask` repo's bar. This personal tap holds the formula until that changes. The cask itself is otherwise standard — when NetAudit eventually gets a Developer ID + notarization, the formula moves to main with just the `postflight` block removed.

Source: <https://github.com/sreebalakrishnan/netaudit>
