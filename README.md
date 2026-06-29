# VaultCode 🔐

**A simple password-based text encryptor — encode a message, decode it back, all in your browser.**

VaultCode is a Streamlit web app that turns the classic "encrypt/decrypt with a password" idea into something you can actually use without touching a terminal. Built originally as a desktop Tkinter app, then rebuilt as a web app so anyone can try it from a link.

🔗 **Live app:** [vaultcode.streamlit.app](https://vaultcode.streamlit.app)

---

## What it does ✨

- 🔒 **Encrypt** any text message using a password of your choice
- 🔓 **Decrypt** it back — same message, same password, original text returned
- 🌐 **Runs entirely in the browser** via Streamlit, no install needed to try it
- 🎨 Clean, minimal UI — message box, password field, mode toggle, done

## How it works 🧩

VaultCode uses [Fernet](https://cryptography.io/en/latest/fernet/) symmetric encryption from Python's `cryptography` library. Your password is hashed (SHA-256) to derive an encryption key, which Fernet then uses to encrypt or decrypt your message. The result is base64-encoded so it's safe to copy, paste, or send as plain text.

```
message + password → SHA-256 → Fernet key → encrypted token → base64 string
```

## Tech stack 🛠️

| Layer | Tech |
|---|---|
| App framework | Streamlit |
| Encryption | `cryptography` (Fernet) |
| Deployment | Streamlit Cloud |

## Running it locally 🚀

```bash
git clone https://github.com/zain-the-npc/VaultCode.git
cd VaultCode
pip install -r requirements.txt
streamlit run app.py
```

## Screenshots 📸


![VaultCode screenshot 2](screenshots/vc_ss_02.png)


## Use cases 💡

- Send a sensitive note over chat or email without it being readable in plain text
- Quick personal encryption for notes, passwords, or reminders you want to keep private
- A hands-on way to see symmetric encryption in action — type a message, watch it transform, decode it right back.

## Why this exists 💭

Made for fun as a side project — a simple, practical way to explore how password-based encryption works end to end, then ship it as something other people could actually open and try.
