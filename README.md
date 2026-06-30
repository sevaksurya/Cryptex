# 🔐 Text Encryption & Decryption

A sleek, browser-based AES encryption and decryption tool with a cyberpunk Matrix-inspired aesthetic. No server required — everything runs client-side.

![HTML](https://img.shields.io/badge/HTML-5-orange?style=flat-square&logo=html5)
![CSS](https://img.shields.io/badge/CSS-3-blue?style=flat-square&logo=css3)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6-yellow?style=flat-square&logo=javascript)
![CryptoJS](https://img.shields.io/badge/CryptoJS-4.1.1-green?style=flat-square)

---

## ✨ Features

- 🔒 **AES Encryption** — Powered by [CryptoJS 4.1.1](https://cdnjs.cloudflare.com/ajax/libs/crypto-js/4.1.1/crypto-js.min.js) for strong, password-based encryption
- 🔓 **AES Decryption** — Instantly reverse encrypted ciphertext with the correct key
- 🌧️ **Matrix Rain Animation** — Animated falling characters rendered on a full-screen canvas
- 💻 **Terminal-style UI** — Hacker-themed interface with glowing green text, scan lines, and a dark theme
- ⌨️ **Typing Animation** — Output is revealed character by character for a cinematic effect
- 📋 **Console Log Panel** — Displays real-time status messages (`Encryption successful`, `Decryption failed`, etc.)
- 🧑‍💻 **Fully Client-Side** — No backend, no data leaves your browser

---

## 🚀 Live Website

> [Cryptex](https://mango-flower-0a8025d10.4.azurestaticapps.net/) hosted in Azure Static Web Apps.

---

## 📂 Project Structure

```
├── index.html        # Main (and only) file — HTML, CSS, and JS are all inline
└── README.md         # You're reading it
```

---

## 🛠️ How to Use

### Encrypt Text
1. Type or paste your message into the **text area**
2. Enter a **secret key** (password) in the key field
3. Click **Encrypt**
4. Wait for the typing animation — your AES ciphertext will appear below

### Decrypt Text
1. Paste the **encrypted ciphertext** into the text area
2. Enter the **same secret key** used during encryption
3. Click **Decrypt**
4. Your original plaintext will be revealed

> ⚠️ **Important:** The key must match exactly. If the key is wrong, decryption will return `Invalid decryption key or text`.

---

## 🔧 Dependencies

| Library | Version | Source |
|---------|---------|--------|
| [CryptoJS](https://github.com/brix/crypto-js) | 4.1.1 | jsDelivr CDN |
| [Inconsolata Font](https://fonts.google.com/specimen/Inconsolata) | — | Google Fonts |

No npm, no build step. Both dependencies are loaded via CDN.

---

## 🔐 Security Notes

- Encryption uses **AES (Advanced Encryption Standard)** via CryptoJS, which employs a PBKDF-style key derivation internally
- This tool is intended for **lightweight, educational use** — not for securing highly sensitive production data
- Since everything runs in the browser, there is **no server-side logging** of your text or key
- Always use a **strong, unique key** for meaningful security

---

## 🖥️ Browser Compatibility

| Browser | Supported |
|---------|-----------|
| Chrome | ✅ |
| Firefox | ✅ |
| Edge | ✅ |
| Safari | ✅ |
| Opera | ✅ |

---

## 🙌 Acknowledgements

- [CryptoJS](https://github.com/brix/crypto-js) by Jeff Mott for the cryptographic library
- Matrix rain animation inspired by the iconic *The Matrix* digital rain effect
- Font: [Inconsolata](https://fonts.google.com/specimen/Inconsolata) via Google Fonts

## License

This project is licensed under the [MIT License](LICENSE).

