# NETWORKWALKS-B083-WK3



https://github.com/user-attachments/assets/c4a56b59-460c-4489-8b08-67348f2cb6a0





Week 3 project submissions for the NetworkWalks Cybersecurity & Ethical Hacking course — **Password Cracking**, covering two lab modules that recover the password of a protected PDF file using different tools and approaches.

## 📁 Repository Structure

```
NETWORKWALKS-B083-WK3/
├── PM1-JOHNTHERIPPER/          # Project Module 1: Password cracking with John the Ripper
├── PM2-NETWORKWALKS TOOLS/     # Project Module 2: Password cracking with NetworkWalks online tools
└── .gitignore
```

---

## 📌 Project Module 1 — Password Cracking with John the Ripper (JTR)

**Objective:** Recover the password of a protected PDF file (`My Locked PDF1.pdf`) using John the Ripper (John and/or Johnny GUI).

**Tools:**
- John the Ripper (CLI) — pre-installed on Kali Linux
- `pdf2john` — extracts a crackable hash from a password-protected PDF

**Approach:**
1. Extract the PDF's password hash locally using `pdf2john`.
2. Run John the Ripper against the extracted hash using a dictionary/wordlist attack.
3. Retrieve the cracked password with `john --show`.
4. Open the PDF using the recovered password to confirm success.

**Result:** Password recovered — `password1`

📄 See [`PM1-JOHNTHERIPPER`](./PM1-JOHNTHERIPPER) for the full report and supporting files.

---

## 📌 Project Module 2 — Password Cracking with NetworkWalks Tools

**Objective:** Recover the password of the same protected PDF file (`My Locked PDF1.pdf`) using two free, browser-based tools built by NetworkWalks — without installing any software.

**Tools:**
- [NetworkWalks Hash Calculator](https://networkwalks.com/hash-calculator/) — extracts a crackable `$pdf$...` hash from a locked PDF, processed locally in the browser
- [NetworkWalks Password Cracker](https://networkwalks.com/password-cracker/) — runs a dictionary attack against the extracted hash

**Approach:**
1. Upload the locked PDF to the Hash Calculator to extract its hash.
2. Copy the full `$pdf$...` hash value.
3. Paste the hash into the Password Cracker and start the dictionary attack.
4. Use the cracked password to open the PDF and confirm success.

**Result:** Password recovered — `password1`

📄 See [`PM2-NETWORKWALKS TOOLS`](./PM2-NETWORKWALKS%20TOOLS) for the full report and supporting files.

---

## 🎓 Key Concepts Learned

- **Encryption vs. Hashing** — Encryption is reversible with the correct key; hashing is a one-way function used to verify rather than reveal data.
- **Password hash extraction** — Protected files (PDF, ZIP, Office docs) store password verification data as a hash, which must be extracted before it can be attacked.
- **Dictionary attacks** — Cracking tools try candidate passwords from a wordlist against the hash until a match is found.
- **Password strength matters** — Simple, common passwords like `password1` are cracked almost instantly, regardless of whether a local CLI tool or an online tool is used.

---

## ⚠️ Disclaimer

This repository contains coursework completed for educational purposes as part of the NetworkWalks Cybersecurity & Ethical Hacking training program. All password cracking was performed on a sample file explicitly provided for lab practice. These techniques should only be used on systems and files you own or have explicit authorization to test.

---

## 🔗 References

- [John the Ripper — Openwall](https://www.openwall.com/john/)
- [Johnny GUI — Openwall](https://openwall.info/wiki/john/johnny)
- [NetworkWalks Academy](https://www.networkwalks.com)



