# Sampatti — releases

**Sampatti** adds up everything you own (and owe) into one honest number, explains it in
plain words, and — when you ask — lets an AI look it over. It's a desktop app for macOS and
Windows, India-first, with a US market mode built in.

**Your money stays on your computer.** Imports, holdings, net worth, history — all of it
lives only on your machine. The optional AI review sends just a small, previewable summary of
totals and percentages to Claude (never your statements), either through a relay or with your
own Anthropic API key.

---

## Install

### macOS (Apple Silicon — M-series, macOS 11+)

1. Download `Sampatti_<version>_aarch64.dmg` from the [Releases page](../../releases).
2. Open it and **double-click Sampatti**.
3. It offers to **move itself into Applications** — click yes, and it reopens from there.

No dragging, no Homebrew. The app is signed with an Apple Developer ID and notarized by
Apple, so it opens normally on first launch — no security warnings. From here on it
**auto-updates**: it checks for a newer signed release and installs it in place (Settings →
Check for updates, or automatically on launch).

### Windows (10/11, x64)

Download the latest `Sampatti_<version>_x64-setup.exe` from the [Releases page](../../releases)
and run it. This build is unsigned, so SmartScreen will warn once — click
**More info → Run anyway**.

**"Is this safe?"** The warning means *unsigned*, not *unsafe* — no paid certificate is used.
Every release attaches proof you can check yourself:

- **Checksum** — make sure the download wasn't tampered with. In PowerShell:
  `certutil -hash Sampatti_<version>_x64-setup.exe SHA256`, then compare to
  `SHA256SUMS-windows.txt` on the release.
- **VirusTotal** — the release notes link a scan across ~70 antivirus engines.
- **Build provenance** — the installer is built by public GitHub Actions straight from source.
  With the [GitHub CLI](https://cli.github.com/):
  `gh attestation verify Sampatti_<version>_x64-setup.exe --bundle Sampatti_<version>_x64-setup.exe.sigstore.json --repo miteshs/sampatti`

This doesn't remove the SmartScreen prompt — only a paid certificate does — but it lets you
confirm exactly what you're running.

---

## Getting started

About 20 minutes, once. After that, a couple of minutes a month. You don't need to be a
"computer person" — if you're comfortable with your phone and net banking, you're fine.

### 1. Open the app and pick your region

On the welcome screen, choose **India** or **United States**. (Want to see the finished thing
first? Click **Load demo portfolio** for a fully filled-in example, then clear it when you're
ready to start your own.)

### 2. Gather your statements into one folder

Make one folder on your computer and drop in a statement from **each place your money lives**.
No need to organize them — just collect them.

- **🇮🇳 India — the shortcut:** your monthly **NSDL/CDSL CAS email** lists every demat stock
  *and* mutual fund in one file. For purchase costs, also grab the **detailed CAS** from
  *camsonline.com → Statements → CAS*. These are usually password-protected PDFs — the app
  asks for the password when you import and never stores or sends it.
- **🇺🇸 US:** download the **positions CSV** from each brokerage (Schwab, Fidelity, Vanguard…).
- **Everything else:** download the holdings statement from each platform. **Excel or CSV
  files work best**, but PDFs and even phone screenshots are fine too.

> Rule of thumb: if you can download it or photograph it, the app can probably read it. Exports
> that include a *cost basis / buy value* column give you true profit-and-loss.

### 3. Import the folder

Click **Add data → 📁 Import a whole folder** (or **Import files** for individual ones).

Each statement turns into a **card for you to check** — the account name, the amounts, anything
that looks off. **Nothing is saved until you approve each card.** You're always in control.

Next month, import the newer statement and it simply **updates** that account — it won't create
a duplicate.

### 4. Add the things that don't come as statements

Some assets have no download. Add these by hand on the **Holdings** screen:

- **India:** your house, PF, FDs, insurance, gold — and any **loans**, so the total is honest.
- **US:** your house, 401(k)/IRA, CDs, insurance — and any **loans**.

Everything stays editable later (Manage → ✎).

### 5. Bring values up to today

Click **Refresh live prices** on the Holdings screen. The app also quietly records your net
worth each day you open it, so a **personal history chart builds itself** over time.
(If you hold US assets, refresh the USD→INR rate in Settings.)

### 6. Connect Claude for the AI review

Go to the **Settings** tab → **AI analysis**:

- **Easiest:** paste the **access code** you were given into *Settings → Access code*. That's
  all the relay needs.
- **Most private:** turn on **Developer mode** and use your own Anthropic API key
  (`platform.claude.com` → API keys), stored in the macOS Keychain / Windows Credential Manager
  and used to call Anthropic directly.

### 7. Ask anything, in your own words

Run the analysis, then ask plain questions like *"Am I too dependent on one stock?"* or
*"Is my mix too risky for my age?"* You get a full read on concentration, diversification, tax,
liquidity and retirement — then follow-ups.

**Your privacy here:** only a small summary of totals and percentages is ever sent — never your
actual statements — and you can **preview exactly what's about to be sent** before anything
leaves your computer.

---

### The one thing to remember

You approve every card, every value, and every message before it counts. The app never does
anything with your money data behind your back — it all lives on this one computer.

## Notes

- macOS: Apple Silicon (M-series), macOS 11+. Windows: 10/11, x64.
- Works fully offline except live prices / FX and AI analysis, which are both optional.
- This repository hosts release artifacts only.
