# Lab 1: Symmetric Encryption Practice

## Objective
Understand and practice encryption and decryption techniques.

## Prerequisites
- Basic understanding of cryptography concepts
- Python or OpenSSL installed

## Tasks

### Task 1: Caesar Cipher (Classical Cryptography)
1. Implement or use a Caesar cipher to encrypt a message
2. Try different shift values
3. Practice breaking the cipher (frequency analysis)

**Python Example:**
```python
def caesar_encrypt(text, shift):
    result = ""
    for char in text:
        if char.isalpha():
            start = ord('A') if char.isupper() else ord('a')
            result += chr((ord(char) - start + shift) % 26 + start)
        else:
            result += char
    return result

message = "HELLO CYBERSECURITY"
encrypted = caesar_encrypt(message, 3)
print(f"Encrypted: {encrypted}")
```

### Task 2: Symmetric Encryption with OpenSSL
1. Create a file with sensitive text
2. Encrypt it using AES-256:
   ```bash
   echo "Sensitive data" > secret.txt
   openssl enc -aes-256-cbc -salt -in secret.txt -out secret.enc -k PASSWORD
   ```
3. Decrypt the file:
   ```bash
   openssl enc -aes-256-cbc -d -in secret.enc -out decrypted.txt -k PASSWORD
   ```
4. Verify the contents match

### Task 3: Base64 Encoding
1. Encode a message to Base64:
   ```bash
   echo "Cybersecurity" | base64
   ```
2. Decode it back:
   ```bash
   echo "Q3liZXJzZWN1cml0eQo=" | base64 -d
   ```
3. Explain why Base64 is NOT encryption

### Task 4: Password Encryption
Create a simple Python script to encrypt/decrypt passwords:
```python
from cryptography.fernet import Fernet

# Generate a key
key = Fernet.generate_key()
print(f"Key: {key.decode()}")

# Create cipher object
cipher = Fernet(key)

# Encrypt
password = b"MySecurePassword123"
encrypted = cipher.encrypt(password)
print(f"Encrypted: {encrypted.decode()}")

# Decrypt
decrypted = cipher.decrypt(encrypted)
print(f"Decrypted: {decrypted.decode()}")
```

## Commands Reference
```bash
openssl enc -aes-256-cbc      # AES encryption
base64                         # Base64 encoding/decoding
md5sum                         # MD5 hash (deprecated for security)
sha256sum                      # SHA-256 hash
```

## Deliverables
1. Screenshots of encryption/decryption processes
2. Working code examples
3. Answers to questions below

## Questions
1. What is the difference between encryption and encoding?
2. Why is Caesar cipher considered weak?
3. What is the key difference between symmetric and asymmetric encryption?
4. Why should you never use MD5 for password hashing?
5. What is a "salt" in cryptography?

## Challenge
Research and explain the difference between AES-128, AES-192, and AES-256. Which is most secure and why?
