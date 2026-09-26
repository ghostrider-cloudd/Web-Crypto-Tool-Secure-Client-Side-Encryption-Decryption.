from pathlib import Path

readme = r"""# 🔐 Cipher Vault

### Secure Client-Side Encryption & Decryption Web Tool

**Cipher Vault** is a modern, browser-based cryptography tool that allows users to encrypt and decrypt text and files directly in their web browser.

It supports **AES-GCM symmetric encryption** and **RSA-OAEP asymmetric encryption**, along with RSA key generation, key import/export, file handling, password-strength analysis, and downloadable encrypted/decrypted output.

All cryptographic operations are performed locally using the **Web Crypto API**.

---

## ✨ Features

### 🔒 AES-GCM Encryption

- AES-GCM symmetric encryption
- 256-bit AES keys
- Password-based key derivation using PBKDF2
- SHA-256 hashing
- Random salt and IV generation
- Text encryption and decryption
- File encryption and decryption

### 🔑 RSA-OAEP Encryption

- RSA 2048-bit key generation
- SHA-256
- Public-key encryption
- Private-key decryption
- Public key import/export
- Private key import/export

### 📁 File Encryption

- File upload
- Drag-and-drop support
- File encryption
- File decryption
- Download encrypted files
- Download decrypted files

### 📊 Password Strength

The AES password field provides a real-time strength indicator based on:

- Password length
- Lowercase characters
- Uppercase characters
- Numbers
- Special characters

### 🛡️ Client-Side Processing

Cipher Vault performs cryptographic operations directly inside the browser.

**No backend server is required for the encryption/decryption process.**

> Never share your private key or encryption password. Losing them may make encrypted data unrecoverable.

---

## 🧰 Technology Stack

| Technology | Purpose |
|---|---|
| HTML5 | Application structure |
| CSS3 | Styling and responsive design |
| JavaScript | Application logic |
| Web Crypto API | Cryptographic operations |
| Tailwind CSS | UI utilities |
| Font Awesome | Icons |
| Google Fonts | Typography |

---

## 🔐 Cryptographic Algorithms

### AES-GCM

AES-GCM is used for password-based symmetric encryption.

```text
Password
   │
   ▼
PBKDF2 + SHA-256
   │
   ▼
256-bit AES Key
   │
   ▼
AES-GCM Encryption
   │
   ▼
Encrypted Data
