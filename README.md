### ✅ Part 3: SSH Encryption & Decryption (OpenSSL)

**Commands used:**
```bash
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

yaml
Copy

---

✅ Let me know if you want me to build you a **GitHub profile README template** next! We can show off your projects, skills, and goals with style.






