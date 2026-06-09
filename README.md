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

## Getting started (5 steps)

1. **Install** (above), launch Sampatti.
2. **Privacy tab** — add your Anthropic API key (stored in the macOS Keychain); refresh the
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
