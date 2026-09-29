# 🔐 Cipher Vault

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
```

The implementation uses:

- AES-GCM
- 256-bit key
- PBKDF2
- SHA-256
- 100,000 PBKDF2 iterations
- Random 16-byte salt
- Random 12-byte IV

### RSA-OAEP

RSA uses a public/private key pair.

```text
             RSA Key Pair
             /          \
            /            \
     Public Key        Private Key
         │                  │
         ▼                  ▼
     Encryption         Decryption
```

The implementation uses:

- RSA-OAEP
- 2048-bit modulus
- Public exponent 65537
- SHA-256

> RSA-OAEP is intended for relatively small amounts of data. AES-GCM is more suitable for larger files.

---

## 🖥️ User Interface

Cipher Vault features a modern cybersecurity-inspired interface with:

- Responsive desktop and mobile layout
- Encryption/decryption controls
- Algorithm selection
- Password-strength indicator
- Input/output workspace
- File upload controls
- Drag-and-drop support
- RSA key management
- Security information
- Algorithm information
- Accessible controls and focus states

---

## 📋 Supported Operations

| Operation | AES-GCM | RSA-OAEP |
|---|:---:|:---:|
| Text Encryption | ✅ | ✅ |
| Text Decryption | ✅ | ✅ |
| File Encryption | ✅ | ⚠️ Limited |
| File Decryption | ✅ | ⚠️ Limited |
| Password-Based Encryption | ✅ | ❌ |
| Public/Private Keys | ❌ | ✅ |
| Key Generation | ❌ | ✅ |
| Key Import | ❌ | ✅ |
| Key Export | ❌ | ✅ |

---

## 🚀 Getting Started

### Clone the Repository

```bash
git clone https://github.com/ghostrider-ckoudd/web-crypto-tool.git
cd web-crypto-tool
```

### Run Locally

Since Cipher Vault is a static web application, you can open `index.html` directly in a modern browser.

Alternatively, use a local server:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

---

## 📂 Project Structure

```text
web-crypto-tool/
│
├── index.html
└── README.md
```

The application is implemented as a single HTML file containing the HTML structure, CSS styling, and JavaScript functionality.

---

## 📖 How to Use

### Encrypt Text with AES-GCM

1. Select **Encrypt**
2. Select **AES-GCM**
3. Enter a strong password
4. Enter or paste your text
5. Click **Encrypt**
6. Copy or download the encrypted output

### Decrypt Text with AES-GCM

1. Select **Decrypt**
2. Select **AES-GCM**
3. Enter the same password
4. Paste the encrypted Base64 data
5. Click **Decrypt**

### Encrypt Using RSA-OAEP

1. Select **Encrypt**
2. Select **RSA-OAEP**
3. Generate or import an RSA public key
4. Enter your data
5. Click **Encrypt**

### Decrypt Using RSA-OAEP

1. Select **Decrypt**
2. Select **RSA-OAEP**
3. Provide the corresponding private key
4. Paste the encrypted data
5. Click **Decrypt**

---

## 📁 File Encryption

To encrypt a file:

1. Select **Encrypt**
2. Select **AES-GCM**
3. Enter a password
4. Upload a file or drag it into the input area
5. Click **Encrypt**
6. Download the encrypted file

Encrypted files use the `.enc` extension.

---

## 🔑 RSA Key Management

Cipher Vault allows users to:

- Generate a new RSA key pair
- View the public key
- View the private key
- Import public keys
- Import private keys
- Export public keys
- Export private keys

Keep private keys secure and never share them with untrusted parties.

---

## ⚠️ Security Considerations

Cipher Vault is a client-side cryptography project.

Important considerations:

- Use strong, unique passwords.
- Never share private keys.
- Keep backups of important private keys.
- Losing a password or private key can make encrypted data unrecoverable.
- Use AES-GCM for larger data rather than direct RSA encryption.
- Review your security requirements before using the application for highly sensitive production data.

---

## 🌐 Browser Compatibility

Cipher Vault requires a modern browser with Web Crypto API support.

Recommended browsers include:

- Google Chrome
- Microsoft Edge
- Mozilla Firefox
- Safari
- Modern Chromium/WebKit/Gecko-based browsers

---

## 🔭 Future Improvements

Potential improvements include:

- Hybrid RSA + AES encryption
- Secure encrypted file containers
- Key fingerprint verification
- Improved error handling
- Password visibility toggle
- Progressive Web App support
- Offline installation
- Additional cryptographic algorithms
- Advanced file metadata handling

---

## 👨‍💻 Author

**Arjun Mehandrakar**

### Connect

- LinkedIn: https://www.linkedin.com/in/rjunm/
- Email: arjunmehandrakar06@gmail.com

---

## 📄 License

Add your preferred open-source license before publishing the repository.

For example:

```text
MIT License
```

If you choose the MIT License, add a `LICENSE` file containing the standard MIT License text.

---

## 🤝 Contributing

Contributions, suggestions, and improvements are welcome.

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test the application
5. Commit your changes
6. Open a pull request

Example:

```bash
git checkout -b feature/your-feature
git add .
git commit -m "Add your feature"
git push origin feature/your-feature
```

---

## ⭐ Support

If you find **Cipher Vault** useful, consider giving the repository a ⭐ on GitHub.

---

### 🔐 Cipher Vault

**Encrypt locally. Decrypt locally. Keep your keys yours.**
