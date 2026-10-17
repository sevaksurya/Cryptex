# 🔐 Cryptex

Cryptex is a browser-based AES text encryption and decryption tool with a cyberpunk, Matrix-inspired interface. It runs entirely in the browser, so no server or build process is required.

![HTML](https://img.shields.io/badge/HTML-5-orange?style=flat-square&logo=html5)
![CSS](https://img.shields.io/badge/CSS-3-blue?style=flat-square&logo=css3)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6-yellow?style=flat-square&logo=javascript)
![CryptoJS](https://img.shields.io/badge/CryptoJS-4.1.1-green?style=flat-square)

## ✨ Features

- 🔒 **AES encryption** using [CryptoJS 4.1.1](https://github.com/brix/crypto-js)
- 🔓 **AES decryption** with validation for invalid keys and corrupted ciphertext
- 🧩 **Single Mode** for encrypting or decrypting one text value at a time
- 📊 **Bulk Mode** for processing multiple note/text rows in one operation
- 📋 **Clipboard tools** for copying single results, individual bulk rows, or the complete bulk table
- 📥 **Bulk import** from clipboard, comma-separated CSV data, or hyphen-separated text lines
- 📤 **Bulk export** as `cipher_data.txt` or `cipher_data.csv`
- ✍️ **Move Output to Input** for quickly chaining encryption and decryption operations
- ⏳ **CLI-style progress indicator** during encryption and decryption
- 🖥️ **Timestamped terminal log** with informational, success, warning, and error messages
- 🔊 **Optional Web Audio SFX** for clicks, progress ticks, success, and error feedback; muted by default
- 🌧️ **Matrix rain animation**, glowing terminal output, scan lines, and hacker-style grid background
- 📱 **Responsive layout** for desktop and mobile browsers
- 🔐 **Client-side only** — plaintext, ciphertext, and keys are not sent to a backend

## 🚀 Live Website

> [Open Cryptex](https://mango-flower-0a8025d10.4.azurestaticapps.net/)
> Hosted with Azure Static Web Apps.

## 📂 Project Structure

```text
├── index.html        # Main (and only) file - Application markup, styles, and JavaScript
├── README.md         # You're reading it
└── LICENSE           # MIT License
```

## 🛠️ How to Use

### Single Mode

1. Enter an encryption key in the **Encryption key** field.
2. Enter or paste text into the input area.
3. Select **Encrypt** to generate AES ciphertext, or **Decrypt** to recover plaintext.
4. Use **Copy to Clipboard** to copy the result.
5. Use **Move Output to Input ↑** to place the current result back into the input area.

Both operations display an inline progress bar and reveal the result with a terminal-style typing animation. Decryption failures are reported in the status banner and terminal log.

### Bulk Mode

1. Select **Bulk Mode**.
2. Enter the encryption key.
3. Add rows with **+ Add Row**, or use **Paste CSV / TXT** to load multiple rows.
4. Enter a note and the text to encrypt or decrypt for each row.
5. Select **Bulk Encrypt** or **Bulk Decrypt**.
6. Copy individual row results, copy the full table, or download the table as TXT or CSV.

Bulk rows use the following formats:

- **TXT / clipboard format:** `Note - Text`
- **CSV format:** a `Note,Text` header followed by quoted CSV rows

Bulk decryption marks rows that fail with an invalid key or corrupted ciphertext. Select **Edit Inputs** to return to editable input fields, or **Reset** to clear the table and start again. Two empty rows are provided when Bulk Mode is initialized.

### Interface Controls

- **[SFX: OFF] / [SFX: ON]** toggles optional browser-generated sound effects.
- **[Clear Log]** clears the timestamped terminal log.
- **Copy to Clipboard** and bulk copy controls use the browser clipboard when available, with a compatibility fallback.

## 🔧 Dependencies

| Library | Version | Source |
|---------|---------|--------|
| [CryptoJS](https://github.com/brix/crypto-js) | 4.1.1 | [jsDelivr CDN](https://cdn.jsdelivr.net/npm/crypto-js@4.1.1/crypto-js.js) |
| [Inconsolata](https://fonts.google.com/specimen/Inconsolata) | — | Google Fonts |

There is no npm dependency installation and no build step. The two external dependencies are loaded from CDNs by [index.html](index.html).

## ▶️ Run Locally

Because the application is a single static HTML file, it can be opened directly in a browser:

```text
Open index.html
```

For local development, serve the project directory with any static file server and open the resulting URL. An internet connection is required for the CryptoJS and Google Fonts CDN resources unless they are self-hosted.

## 🔐 Security Notes

- Cryptex performs encryption and decryption locally in the browser using CryptoJS AES passphrase-based encryption.
- No application backend receives the entered text, encryption key, or generated ciphertext.
- The encryption key is not stored by the application. Use a strong, unique key and keep it private.
- This project is intended for lightweight or educational use. For highly sensitive data, use a reviewed encryption solution with an appropriate key-management process.
- Client-side encryption cannot protect data if the browser environment or device is compromised.

## 🖥️ Browser Compatibility

Cryptex uses standard browser APIs including Canvas, Web Audio, Blob downloads, and clipboard APIs. Current versions of the following browsers are supported:

| Browser | Supported |
|---------|-----------|
| Chrome | ✅ |
| Firefox | ✅ |
| Edge | ✅ |
| Safari | ✅ |
| Opera | ✅ |

Clipboard read access may be restricted in embedded or insecure contexts. In that case, Bulk Mode provides a manual paste drawer.

## 🙌 Acknowledgements

- [CryptoJS](https://github.com/brix/crypto-js) by Jeff Mott
- Matrix rain animation inspired by *The Matrix* digital rain effect
- [Inconsolata](https://fonts.google.com/specimen/Inconsolata) via Google Fonts

## License

This project is licensed under the [MIT License](LICENSE).
