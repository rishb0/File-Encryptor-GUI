# File Encryptor GUI

A Java-based file encryption and decryption tool with a graphical interface. Supports any file type and uses a split-key system where the encryption key is divided into two separate parts.

---

## Features

- Encrypt and decrypt any file type
- Split-key system — key is divided into two 6-character parts
- Built-in key generator with one-click copy for each key part
- Simple graphical interface built with Java Swing

---

## How It Works

1. A file is read from disk and converted to a Base64 string
2. The string is encrypted using DES in ECB mode
3. The encrypted result is written back to the original file path
4. Decryption reverses this process using the same key parts

### Key System

The key is split into two 6-character parts. Both parts must be provided together to encrypt or decrypt a file. This allows two parties to each hold one half of the key independently.

---

## How to Use

Compile:

```bash
javac FileEncodeGUI.java
```

Run:

```bash
java FileEncodeGUI
```

1. Click **Generate Sample Key** to generate a key and save both parts
2. Click **Encrypt File** to select a file and encrypt it using your key parts
3. Click **Decrypt File** to restore the original file using the same key parts

---

## Requirements

- Java 8 or higher
- No external dependencies — uses only the Java standard library

---

## Security Notice

This project uses DES with ECB mode for demonstration purposes. DES is considered cryptographically weak by modern standards and should not be used to protect sensitive data in production environments.

---

## Author

**Rishabh Soni**