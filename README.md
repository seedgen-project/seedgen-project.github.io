# SeedGen 3

**Live site: https://seedgen3.com**

An offline, open-source BIP-39 seed phrase generator built on two principles:

- **Trust None** — no proprietary hardware, no black-box firmware, no opaque
  key-derivation logic. The whole tool is one readable HTML file. Anyone, even
  without programming knowledge, can read it or paste it into an AI and have it
  audited in minutes.
- **Bring Your Own Entropy** — the randomness comes from *your* world: dice,
  coin flips, a pasted bit string, or live microphone ambient noise, XOR-ed with
  the browser's CSPRNG. Not a number computed on a chip you cannot inspect.

The output is a standard BIP-39 mnemonic. Restore it into any wallet — software
or hardware (Ledger, Trezor, SeedSigner, Krux, …).

## The tool

[`Script/SeedGen_3.html`](Script/SeedGen_3.html) — a single self-contained file.
The QR library and the full BIP-39 word list are embedded; it makes no network
requests.

- Input by words (with BIP-39 dictionary + checksum validation), numbers, or bits
- Physical entropy from the microphone, filtered on measured entropy and checked
  live against NIST SP 800-90B health tests (RCT/APT)
- Private keys and addresses for Bitcoin (Native SegWit, Legacy, Nested SegWit,
  Taproot), Ethereum/EVM and TRON
- Export as QR code, alphanumeric text, or numbers
- Steganographic "decoy label" to camouflage the seed inside an innocuous image
- A startup self-check that verifies the cryptographic core against known test
  vectors on every page load, and locks the UI if it fails

## How to use it

1. Download [`Script/SeedGen_3.html`](Script/SeedGen_3.html) (or get it from the
   [Free Download](https://seedgen3.com/FreeDownload.html) page).
2. **Go offline** — disconnect the network.
3. Open the file in a browser.
4. When you are done, close the browser.

## How to verify it

- Read the source — it is one file, plain HTML/JS, no build step, no dependencies.
- Or paste it into an AI and ask it to audit it.
- Independent AI security audits (DeepSeek, Claude, ChatGPT, Gemini) and the exact
  prompt used are published on the
  [Docs &amp; Reviews](https://seedgen3.com/Docs_Reviews.html) page.

## This repository

This repo *is* the website (served via GitHub Pages). The site pages are the HTML
files at the root; the tool itself is `Script/SeedGen_3.html`.

---

&copy; SeedGen 3 Project. All rights reserved.
