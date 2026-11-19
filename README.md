# NETWORKWALKS-Tin_Maung_Soe--YOUR-BATCH--WK3-PASSWORD-CRACKING

# Password Cracking Lab: John the Ripper (JTR) & Networkwalks Tools

**Week 3 Cybersecurity & Ethical Hacking Project (PM1 & PM2)**  
**Program:** Networkwalks Cybersecurity Internship  
**Instructor:** Waqas Karim (CCIE)  

---

## 📋 Project Overview
This project demonstrates how password hashes work, why weak passwords pose a major security risk, and how security professionals audit file security. In this two-part lab, I extracted the cryptographic hash from an encrypted PDF file (`My Locked PDF1.pdf`) and performed dictionary attacks using two different toolsets:
1. **Project Module 1 (PM1):** John the Ripper (JTR) CLI & Johnny GUI on Windows.
2. **Project Module 2 (PM2):** Networkwalks Browser-Based Hash Calculator & Password Cracker.

> **Disclaimer:** *This lab was conducted strictly for educational and ethical hacking training purposes on authorized lab files provided by Networkwalks Academy.*

---

## 🛠️ Tools & Environment Used
* **Operating System:** Windows 10/11
* **Module 1 Tools:** John the Ripper (`john-1.9.0-jumbo-1-win64`), Johnny GUI (`v2.2`), PDF Hash Extractor (`pdf2john`)
* **Module 2 Tools:** Networkwalks Hash Calculator & Networkwalks Dictionary Password Cracker

---

## 🚀 Execution Steps

### Part 1: Password Cracking with John the Ripper & Johnny GUI (WK3-PM1)
1. **Tool Setup:** Downloaded and extracted `John the Ripper (Jumbo)` and installed the `Johnny` GUI on Windows.
   ![Extracting JTR]
   <img width="560" height="464" alt="2" src="https://github.com/user-attachments/assets/8dcaeeb1-2694-46ca-b1e7-7e3104801700" />

2.**Configuring Johnny:** Opened Johnny Settings and linked the executable path to `john.exe` inside the `/run` directory.
 <img width="694" height="542" alt="3" src="https://github.com/user-attachments/assets/2f9c50b4-f5fe-4486-86fc-b8fa211f2528" />

   
   
3. **Hash Extraction:** Extracted the `$pdf$...` hash from `My Locked PDF1.pdf` (pdf2john format) and saved it locally as `hash1.txt`.
 <img width="1133" height="638" alt="5" src="https://github.com/user-attachments/assets/a892e4e9-1eb5-4a58-924a-45f8f95c07de" />



4. **Dictionary Attack:** Loaded `hash1.txt` into Johnny and started the attack, successfully recovering the plaintext password (`password1`).
 <img width="696" height="545" alt="7" src="https://github.com/user-attachments/assets/b4d09fa4-05c5-4080-9ba8-cfad273136f7" />


---

### Part 2: Password Cracking with Networkwalks Web Tools (WK3-PM2)
1. **Local Hash Extraction:** Uploaded `My Locked PDF1.pdf` into the **Networkwalks Hash Calculator**, which parsed the file locally in the browser and extracted the 128-bit R4/V4 `$pdf$` hash.
   <img width="1525" height="725" alt="01" src="https://github.com/user-attachments/assets/3bc2be41-8c0a-4120-953a-f537a33d294c" />

2. **Running the Dictionary Attack:** Pasted the extracted `$pdf$` hash into the **Networkwalks Password Cracker** using the built-in wordlist.
   <img width="1534" height="725" alt="02" src="https://github.com/user-attachments/assets/005f08c1-1ab5-4d2a-bc1a-fa2ae8644189" />

3. **Password Recovered:** Executed the attack and matched the hash in seconds, revealing the password: `password1`.
   <img width="1530" height="726" alt="03" src="https://github.com/user-attachments/assets/51ccc06a-9f5f-494c-a61f-a1b39356ebce" />

4. **Verification & Flag Capture:** Unlocked the protected PDF using the recovered password to verify access and capture the lab flag.
   <img width="1529" height="686" alt="04" src="https://github.com/user-attachments/assets/1c6ddc60-616b-4c86-a7ee-f602a81dcb3e" />


---

## 🔐 Key Takeaways & Security Lessons
* **Hashing vs. Encryption:** Encryption is a two-way process reversible with a key, whereas hashing is a one-way mathematical function. Attackers don't "decrypt" hashes—they hash wordlist guesses until a digest matches.
* **Defense Against Dictionary Attacks:** Common, short, or dictionary-based passwords (like `password1`) can be cracked almost instantaneously. Enforcing strong password policies (12+ characters with mixed uppercase, lowercase, numbers, and symbols) exponentially increases cracking time and mitigates brute-force/dictionary threats.
