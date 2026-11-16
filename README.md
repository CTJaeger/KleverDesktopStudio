# Klever Desktop Studio

The power wallet for the KleverChain — self-custodial, for Windows, macOS and Linux.

This repository holds **installers only**. The source code is not published.

## Download

| System | Installer (recommended) | Portable |
|---|---|---|
| Windows 10 / 11, 64-bit | [KleverDesktopStudio-win-Setup.exe](https://github.com/CTJaeger/KleverDesktopStudio/releases/latest/download/KleverDesktopStudio-win-Setup.exe) | [KleverDesktopStudio-win-Portable.zip](https://github.com/CTJaeger/KleverDesktopStudio/releases/latest/download/KleverDesktopStudio-win-Portable.zip) |
| macOS 10.15+, Intel and Apple Silicon (Rosetta 2) | [KleverDesktopStudio-macos-x64.pkg](https://github.com/CTJaeger/KleverDesktopStudio/releases/latest/download/KleverDesktopStudio-macos-x64.pkg) | [KleverDesktopStudio-macos-x64.tar.gz](https://github.com/CTJaeger/KleverDesktopStudio/releases/latest/download/KleverDesktopStudio-macos-x64.tar.gz) |
| Linux x64, Debian / Ubuntu / Mint | [KleverDesktopStudio-linux-x64.deb](https://github.com/CTJaeger/KleverDesktopStudio/releases/latest/download/KleverDesktopStudio-linux-x64.deb) | [KleverDesktopStudio-linux-x64.tar.gz](https://github.com/CTJaeger/KleverDesktopStudio/releases/latest/download/KleverDesktopStudio-linux-x64.tar.gz) |

These links always point to the newest release. Every release page lists the
SHA-256 checksums (`SHA256SUMS.txt`); check a download with `sha256sum <file>`
(Linux/macOS) or `certutil -hashfile <file> SHA256` (Windows).

**The installers are not code-signed.** Windows SmartScreen and macOS Gatekeeper will warn.
Windows: "More info" → "Run anyway". macOS: on first start right-click the app → "Open".
Linux: `sudo apt install ./KleverDesktopStudio-linux-x64.deb` installs to `/opt` with a
menu entry. The portable archive (Gentoo, Arch, …) includes `install-shortcut.sh` for a
menu entry.

**Updates:** the app tells you about new releases and installs them on click. Windows
(Setup) replaces itself and restarts. Linux (`.deb`) asks for your password through the
system dialog, installs and restarts. macOS (`.pkg`) opens the system installer. Portable
versions download the archive and open the folder.

**Coming from version 1.x?** Version 2 is a complete rewrite. Back up your wallets
(recovery phrase / PEM export) before you migrate.

## What is in it

- **Encrypted multi-wallet vault** — AES-256-GCM, unlocked with your password
- **Send** — multi-asset send, group send, Claim ALL
- **Mass distribution** — with on-chain snapshots
- **Staking** — batch freeze / delegate / undelegate, validator matchmaking
- **Swap** — built-in DEX swap with price charts and pool-liquidity protection
- **Validator** — manage your validator, own node support
- **Multisig** — account permissions, KleverScan-compatible
- **Watch-only accounts** — with on-behalf signing
- **Governance** — vote on and create network proposals
- **Portfolio** — history and allocation, rebuilt from your transactions
- **Asset owners** — FPR / KDA pool deposits
- **Tax export** — CSV of your full history

## Privacy

- Your keys stay on your own computer, encrypted with your password. They are never sent
  anywhere. There is no telemetry.
- The app talks to the KleverChain API and node of the network you choose (Mainnet,
  Testnet or your own node), to the Klever multisign service when you use multisig, to
  `api.bitcoin.me` for swap quotes, pools and prices, and, for the update check, to
  `github.com` / `api.github.com`. GitHub sees your IP address when the app checks for
  updates or when you download a file; see
  [GitHub's Privacy Statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement).
- Explorer links open KleverScan in your browser.

## License and disclaimer

Freeware — see [LICENSE.txt](LICENSE.txt). The software is provided **as is**, without
warranty of any kind. You alone are responsible for your keys, passwords, backups and
transactions. Transactions on a blockchain cannot be reversed.

Klever, KleverChain, KleverScan and bitcoin.me are names of their respective projects; this
wallet is an independent application and is not affiliated with them.
