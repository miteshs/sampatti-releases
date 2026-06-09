# Sampatti — releases

**Sampatti** is a private, India-first portfolio-analysis app for macOS. All portfolio
data stays on your device — imports, holdings, net worth, history. The optional AI
analysis sends only a compact, previewable summary to Claude, using **your own
Anthropic API key** (stored in the macOS Keychain).

## Install

```sh
brew tap miteshs/sampatti
brew install --cask sampatti
```

Or download the `.dmg` from [Releases](../../releases) and drag **Sampatti** into
*Applications*. The build is currently unsigned, so on a manual install macOS will warn on
first launch — right-click the app → **Open** (the brew cask handles this automatically).

## Notes

- Apple Silicon (M-series) Macs, macOS 10.15+.
- Works fully offline except live prices/FX (optional) and AI analysis (your own key).
- This repository hosts release artifacts only.
