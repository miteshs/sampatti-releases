# Sampatti — releases

**Sampatti** is a private, India-first portfolio-analysis app for macOS and Windows
(a US market mode is built in). All portfolio data stays on your device — imports,
holdings, net worth, history. The optional AI analysis sends only a compact,
previewable summary to Claude — through a relay, or with **your own Anthropic API
key** (stored in your system keychain).

**See it first** — narrated tutorials with captions (~4 min, every tab + AI setup):
[India demo](../../releases/latest/download/sampatti-demo-india.mp4) ·
[US demo](../../releases/latest/download/sampatti-demo-us.mp4)

## Install — macOS (Apple Silicon)

With Homebrew (recommended — updates arrive with `brew upgrade`):

```sh
# Only if you don't have Homebrew yet (check with: brew --version):
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

brew tap miteshs/sampatti
brew trust miteshs/sampatti     # Homebrew asks this once for third-party taps
brew install --cask sampatti
```

**No Homebrew?** Download the `.dmg` from [Releases](../../releases) and drag
**Sampatti** into *Applications*. The build is currently unsigned, so macOS will warn on
first launch — right-click the app → **Open**; on newer macOS you may also need
*System Settings → Privacy & Security → **Open Anyway*** (the brew cask handles this
automatically).

## Install — Windows (x64)

Download `Sampatti_<version>_x64-setup.exe` from [Releases](../../releases) and run it.
The installer is unsigned, so SmartScreen will warn — click **More info → Run anyway**.

## Notes

- macOS: Apple Silicon (M-series), macOS 11+. Windows: 10/11, x64.
- Works fully offline except live prices/FX (optional) and AI analysis (relay or your own key).
- This repository hosts release artifacts only.

## Getting started (5 steps)

1. **Install** (above), launch Sampatti.
2. **Settings tab** — choose how AI analysis reaches Claude: the relay (easiest — ask us
   for access in [an issue](../../issues)), or your own Anthropic API key for maximum
   privacy (stored in the macOS Keychain / Windows Credential Manager). Refresh the
   USD→INR rate if you hold US assets.
3. **Gather statements** — download a holdings/positions export from every account into one
   folder. Prefer CSV/Excel (parsed fully on-device) and pick exports that include
   *cost basis / buy value* columns so you get true P&L. PDFs/screenshots also work — they're
   read by Claude only after you confirm.
4. **Add data → 📁 Import a whole folder** — review each parsed account before saving: fix
   names/classes/values, fill missing cost bases, and check "Apply to" (New account vs Update
   an existing one). Everything stays editable later (Manage → ✎). Add property/PPF/FDs/gold
   by hand, loans as liabilities, and your income sources.
5. **AI Analysis → ✨ Analyze my portfolio** — preview the exact compact summary being sent,
   get the full concentration/diversification/tax/liquidity/retirement read, then ask
   follow-ups.

Re-import newer statements anytime — they update the matching account instead of duplicating it.
