# Colly Portfolio Releases

> **Download & Verification Guides (12 Languages):** Full download and OpenPGP/SHA-256 verification instructions in all 12 supported languages are available on the official website at https://collyportfolio.1blue.net/download/

Official binary releases and OpenPGP verification manifests for **Colly Portfolio**.

- **Website:** https://collyportfolio.1blue.net
- **Download & Verification Guides (12 Languages):** https://collyportfolio.1blue.net/download/
- **Dual-Origin OpenPGP Public Key:** https://collyportfolio.1blue.net/keys/colly-linux-signing-key.asc (also mirrored in this repository as [`colly-linux-signing-key.asc`](./colly-linux-signing-key.asc))
- **OpenPGP Primary Fingerprint (`Ed25519`):** `821B 62D1 4FE9 CAB7 61FB 29F7 CD1C 01CB A2EB 4425`
- **Signing Subkey Fingerprint (`Ed25519`):** `2353 A93F 05DA 7D54 B1FB 2438 AB7F 9D98 695B 0FF3`

<details>
<summary>Localized Download & Verification Guides (12 Languages)</summary>

- [English](https://collyportfolio.1blue.net/download/en/#linux)
- [简体中文](https://collyportfolio.1blue.net/download/zh-CN/#linux)
- [繁體中文](https://collyportfolio.1blue.net/download/zh-TW/#linux)
- [Español](https://collyportfolio.1blue.net/download/es/#linux)
- [Français](https://collyportfolio.1blue.net/download/fr/#linux)
- [العربية](https://collyportfolio.1blue.net/download/ar/#linux)
- [Русский](https://collyportfolio.1blue.net/download/ru/#linux)
- [한국어](https://collyportfolio.1blue.net/download/ko/#linux)
- [日本語](https://collyportfolio.1blue.net/download/ja/#linux)
- [Tiếng Việt](https://collyportfolio.1blue.net/download/vi/#linux)
- [Português](https://collyportfolio.1blue.net/download/pt/#linux)
- [हिन्दी](https://collyportfolio.1blue.net/download/hi/#linux)

</details>

---

## Linux (`x86_64`) Installation & Verification

> **System compatibility:** Ubuntu 22.04 LTS or later, Debian 12 or later (`x86_64`, `glibc >= 2.34`).
> **Edition:** Free edition (up to 10 non-deleted subscription records per local account; local encrypted storage, export, backup, and manual sync included).

### 1. Verify OpenPGP Signature & SHA-256 Checksums

Download the installer (`.deb` or `.AppImage`), `SHA256SUMS`, and `SHA256SUMS.asc` from the [Latest Release](https://github.com/colly-portfolio/releases/releases/latest), then verify against the public key hosted on the official website:

```bash
curl -fsSL https://collyportfolio.1blue.net/keys/colly-linux-signing-key.asc | gpg --import
gpg --verify SHA256SUMS.asc SHA256SUMS
sha256sum --ignore-missing -c SHA256SUMS
```

Confirm that `gpg --verify` reports a good signature from `Colly Developer (Colly Portfolio Linux Release Signing) <collydeveloper@outlook.com>` matching primary fingerprint `821B 62D1 4FE9 CAB7 61FB 29F7 CD1C 01CB A2EB 4425`.

### 2. Install

- **Debian / Ubuntu (`.deb`):**
  ```bash
  sudo apt install ./Colly-Portfolio-2.0.0-2012-Linux-x86_64.deb
  ```
- **AppImage (`.AppImage`):**
  ```bash
  chmod +x Colly-Portfolio-2.0.0-2012-Linux-x86_64.AppImage
  ./Colly-Portfolio-2.0.0-2012-Linux-x86_64.AppImage
  ```
