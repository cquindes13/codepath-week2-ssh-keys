# Week 2 – All About SSH Keys 🔐  
## CodePath Cybersecurity | Spring 2025

This repository contains my submission for **Week 2** of CodePath’s Cybersecurity course. The project covered the generation and use of SSH keys for authentication, encryption/decryption, and signing Git commits for integrity.

---

## 📁 Contents
- Project submission (PDF/Docx)
- Screenshots of:
  - SSH encryption and decryption steps
  - Git commit and signature verification
  - Stretch challenge: SCP file transfer using SSH keys

---

## 🎯 Learning Objectives
By the end of this project, I was able to:
- Generate and manage SSH key pairs using `ssh-keygen` and `openssl`
- Use SSH public/private key pairs to encrypt and decrypt data
- Sign Git commits and verify commit integrity using SSH key signatures
- Explore additional use cases for SSH such as secure file transfers

---

## 🧪 Project Parts

### ✅ Part 1: SSH Key Generation
Used `ssh-keygen` to generate a 4096-bit RSA key pair:
```bash
ssh-keygen -t rsa -b 4096 -C "CYB101 Ubuntu Key                                                                                  
