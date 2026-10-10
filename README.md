# ◈ Cipher

**Static AES-256 text encryption — 100% in-browser.**

Type a secret, set a password, get encrypted text. Share it or store it.
Only the password unlocks it. Nothing ever leaves your device.

## How it works

- `AES-256-GCM` encryption via the [Web Crypto API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Crypto_API)
- Key derived with `PBKDF2-SHA256`, 600,000 iterations, random 16-byte salt
- Random 12-byte IV per message — encrypting the same text twice gives different output
- Output format: `cipher1.<base64(salt ‖ iv ‖ ciphertext)>`
- Wrong password → decryption fails. There is no backdoor, no recovery.

## Use

Open `index.html` in any modern browser — or serve the folder statically.
No build step, no dependencies, no server. Works offline.

## Files

- `index.html` — the entire app (markup + styles + crypto)

---

Built by [Syed Hussain Raza Wasti](https://github.com/SyedHussainwasti)
