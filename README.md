Here’s an updated `README.md` that reflects the goal of helping users understand the working flow of PKI infrastructure, focusing on how hashing, signatures, encryption, and decryption work:

---

# PKI Workflow Demonstration: Hashing, Signing, and Encryption

## Overview
This Python application is designed to help users understand the working flow of Public Key Infrastructure (PKI). The primary focus is on demonstrating how hash functions, digital signatures, encryption, and decryption work together in secure communications.

### Key Concepts Covered:
- **Hashing**: Learn how a cryptographic hash function generates a fixed-size output from a variable-sized message.
- **Digital Signatures**: Understand how RSA signatures are created and used to ensure data authenticity.
- **Encryption/Decryption**: See how asymmetric encryption (RSA) is applied to securely encrypt and decrypt messages.
- **PKI Workflow**: Explore the basic principles of how PKI infrastructure manages keys and signatures.

## Prerequisites
Ensure the following Python libraries are installed:

- `tkinter` (for GUI)
- `pycryptodome` (for cryptographic operations):
  ```bash
  pip install pycryptodome
  ```

## Purpose
This application is designed for learning purposes to simulate the core components of PKI. The focus is not on creating a fully functional PKI system but rather on demonstrating how the underlying mechanisms work:
- How a **hash function** processes a message.
- How an **RSA signature** can be generated and verified.
- How **encryption** and **decryption** happen using public/private keys.

## How to Run

1. Clone or download the project files.
2. Install the dependencies:
   ```bash
   pip install pycryptodome
   ```
3. Run the Python script:
   ```bash
   python app.py
   ```

## Functionality and Workflow

### 1. Hashing
- **Purpose**: A hash function generates a unique "fingerprint" of the message. This fingerprint is crucial in ensuring the integrity of data.
- **How it Works**: Enter a message in the input field, select the desired hash function, and the application will display the hashed result.

### 2. Digital Signatures
- **Purpose**: A digital signature verifies the authenticity of a message and that it hasn’t been tampered with.
- **How it Works**: 
  - The message hash is signed using a private RSA key.
  - The signature is then displayed, representing the encrypted hash.
  
### 3. Encryption and Decryption
- **Purpose**: Encryption ensures the confidentiality of a message, while decryption restores the original message for the intended recipient.
- **How it Works**:
  - A message (or hash) is encrypted using the recipient's public key.
  - The recipient can decrypt the message using their private key to restore the original content.
  
### 4. Key Generation (RSA)
- **Purpose**: RSA keys (private and public) are generated to secure communications.
- **How it Works**: The application creates an RSA key pair, where the public key is used for encryption and the private key for decryption.

### 5. Verification
- **Purpose**: To verify the integrity and authenticity of the message.
- **How it Works**: The application compares the original message’s hash with the decrypted signature to check if the message has been tampered with.

## User Interface

- **Message Input Field**: Enter your message here.
- **Hash Result**: The output of the hash function applied to the message.
- **Signature Section**: Displays the generated RSA signature for the hashed message.
- **Verification Result**: Shows whether the message has been verified or if it has been altered.
- **Encryption/Decryption**: Demonstrates RSA encryption and decryption steps.

## Educational Focus

This application is best suited for:
- Students or professionals learning about **PKI infrastructure**.
- Understanding the relationship between **hashing**, **signing**, and **encryption**.
- Experimenting with RSA key generation, message signing, and verification in a controlled environment.
