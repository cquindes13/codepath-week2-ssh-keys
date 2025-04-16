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
ssh-keygen -t rsa -b 4096 -C "CYB101 Ubuntu Key"
✅ Part 2: SSH Authentication (optional walkthrough)
Used ssh-copy-id and scp to enable key-based login without a password.

✅ Part 3: SSH Encryption & Decryption (OpenSSL)
Commands used:

bash
Copy
openssl genrsa -out ~/.ssh/privatekey.pem 2048
openssl rsa -in ~/.ssh/privatekey.pem -pubout -out ~/.ssh/publickey.pem
echo "My secret code is CHEESE" > secret.txt
openssl pkeyutl -encrypt -pubin -inkey ~/.ssh/publickey.pem -in secret.txt -out secret.txt.encrypted
openssl pkeyutl -decrypt -inkey ~/.ssh/privatekey.pem -in secret.txt.encrypted -out secret.txt.decrypted
✅ Part 4: Git Commit Signing
Commands used:

bash
Copy
git init
git config --global commit.gpgsign true
git config --global gpg.format ssh
git config --global user.signingkey "<your SSH key>"
git commit --allow-empty --message="Did the SSH signing work?"
git show --show-signature
🏁 Stretch Challenge: Extra SSH Use
Explored how to use SSH keys for SCP file transfers:

bash
Copy
scp -i ~/.ssh/id_rsa_cyb101 example.txt user@localhost:/destination/
💬 Reflection
Q1: SSH in 3 Emojis
😃 😅 😦

Q2: Why use Kali Linux instead of Windows/Mac?
Kali Linux is designed for penetration testing and comes preloaded with security tools. It's open-source, highly customizable, and gives more control over security configurations. It’s a go-to for ethical hackers and cybersecurity professionals.

🙌 Shoutouts
Big thanks to:

Google

ChatGPT 🤖

CyberChef & OpenSSL Docs

🧠 Author Info
Name: Cristian Quindes
Email: quindes1352@gmail.com
Course: CYB101 – CodePath Cybersecurity Spring 2025

vbnet
Copy

---

Once your repo is published, let’s:
- ✅ Pin both Week 1 and Week 2 projects to your GitHub profile
- 🎨 Add a profile README (like a portfolio intro)
- 🏷️ Write a clean summary in the repo’s About section
- 📌 Add tags like: `ssh`, `cybersecurity`, `encryption`, `git`, `openssl`

Let me know when you're ready and I can help you set all that up!
