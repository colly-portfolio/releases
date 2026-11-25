# Colly Portfolio Releases

Official binary releases and OpenPGP verification manifests for **Colly Portfolio**.

- **Website:** https://collyportfolio.1blue.net
- **Dual-Origin OpenPGP Public Key:** https://collyportfolio.1blue.net/keys/colly-linux-signing-key.asc (also mirrored in this repository as [`colly-linux-signing-key.asc`](./colly-linux-signing-key.asc))
- **OpenPGP Primary Fingerprint (`Ed25519`):** `821B 62D1 4FE9 CAB7 61FB 29F7 CD1C 01CB A2EB 4425`
- **Signing Subkey Fingerprint (`Ed25519`):** `2353 A93F 05DA 7D54 B1FB 2438 AB7F 9D98 695B 0FF3`

---

## Linux (`x86_64`) Installation & Verification / 安装与校验

> **System compatibility / 系统要求：** Ubuntu 22.04 LTS or later, Debian 12 or later (`x86_64`, `glibc >= 2.34`).
> **Edition / 版本说明：** Free edition (up to 10 subscription records per local account; local encrypted storage, export, backup, and manual sync included).

### 1. Verify OpenPGP Signature & SHA-256 Checksums

Download the installer (`.deb` or `.AppImage`), `SHA256SUMS`, and `SHA256SUMS.asc` from the [Latest Release](https://github.com/colly-portfolio/releases/releases/latest), then verify against the public key hosted on the official website:

```bash
curl -fsSL https://collyportfolio.1blue.net/keys/colly-linux-signing-key.asc | gpg --import
gpg --verify SHA256SUMS.asc SHA256SUMS
sha256sum --ignore-missing -c SHA256SUMS
```

Confirm that `gpg --verify` reports a good signature from `Colly Developer (Colly Portfolio Linux Release Signing) <collydeveloper@outlook.com>` matching primary fingerprint `821B 62D1 4FE9 CAB7 61FB 29F7 CD1C 01CB A2EB 4425`.

### 2. Install / 安装

- **Debian / Ubuntu (`.deb`):**
  ```bash
  sudo apt install ./Colly-Portfolio-2.0.0-2012-Linux-x86_64.deb
  ```
- **AppImage (`.AppImage`):**
  ```bash
  chmod +x Colly-Portfolio-2.0.0-2012-Linux-x86_64.AppImage
  ./Colly-Portfolio-2.0.0-2012-Linux-x86_64.AppImage
  ```
