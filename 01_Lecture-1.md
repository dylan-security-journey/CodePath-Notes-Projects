# Cybersecurity Notes

## 🔐 CIA Triad
- **Confidentiality** – Ensures that only authorized users can access data.  
  - Methods: authentication, encryption, access controls.  
- **Integrity** – Ensures data is accurate and unaltered.  
  - Methods: checksums, hashing, digital signatures.  
- **Availability** – Ensures systems and data are accessible when needed.  
  - Methods: redundancy, backups, disaster recovery, uptime monitoring.  

---

## ⚙️ Key Concepts

### Processes
- Supply chain connections  
- Business workflows that rely on secure IT systems  

### Systems
- Data collection mechanisms  
- Information flow pipelines (databases, storage, analytics platforms)  

### Technology
- IT systems, networks, and communication infrastructure  

### Facility Assets
- Physical resources such as buildings, land, vehicles, and machinery  

---

## ⚠️ Security Terms

- **Vulnerability** – A weakness or flaw in a system that can be exploited.  
- **Threat** – When an attacker has the capability and opportunity to exploit a vulnerability.  
- **Risk** – The probable frequency and magnitude of loss resulting from a threat exploiting a vulnerability.  

---

## 🚨 Threat Examples

- **Cross-Site Scripting (XSS)** – Discovered in 2016; attackers used malicious DM deeplinks to insert malware.  
- **Social Engineering (Twitter Hack, 2020)** – Attackers phished employees, gained admin access, and compromised accounts like Joe Biden and Barack Obama.  
- **Spam** – High probability, low loss risk.  
- **Account Takeover** – Lower probability but higher loss risk.  

---

## 🧑‍💻 Threat Actors

- **Nation-State Actor** – Government-sponsored hacking groups.  
- **Hacktivist** – Promote political or social change through cyberattacks.  
- **Cybercriminal** – Commit crimes for financial gain (fraud, ransomware, theft).  
- **Insiders** – Employees or individuals within an organization who abuse access.  

---

## 🛡️ Controls

Controls are policies, procedures, or actions designed to **mitigate risk**.  

- **Preventive Controls** – Stop an incident before it occurs.  
  - Examples: firewalls, multi-factor authentication, encryption.  

- **Detective Controls** – Identify incidents as they occur.  
  - Examples: intrusion detection systems, honeypots, log monitoring.  

- **Corrective Controls** – Restore systems after an incident.  
  - Examples: patch management, backups, incident response plans.  

- **Physical Controls** – Restrict access to physical environments.  
  - Examples: locks, guards, cameras, keycards.  

- **Technical Controls** – Use technology to enforce security.  
  - Examples: antivirus software, intrusion prevention systems, honeypots.  

- **Administrative Controls** – Policies, training, and procedures that guide user behavior.  
  - Examples: security awareness training, access review policies, incident response guidelines.  

**Example:**  
Honeypots (technical, detective) are deployed to **attract attackers**, allowing monitoring and detection of malicious activity.  

---

## 📑 NIST Cybersecurity Framework (CSF)

The NIST CSF provides a structured way to **assess and mitigate risk**.  
It includes five core functions:  

1. **Identify** – Understand organizational systems, assets, and risks.  
2. **Protect** – Develop safeguards to secure assets and reduce risk.  
3. **Detect** – Identify security events and anomalies quickly.  
4. **Respond** – Contain and mitigate the impact of an incident.  
5. **Recover** – Restore systems, services, and operations after an incident.  

---

# ✅ Summary

- The **CIA Triad** is the foundation of cybersecurity.  
- Security requires addressing **processes, systems, technology, and facilities**.  
- Risks arise when **threats exploit vulnerabilities**, causing potential loss.  
- **Threat actors** can be external (nation-states, hacktivists, criminals) or internal (insiders).  
- **Controls** mitigate risks through preventive, detective, corrective, physical, technical, and administrative methods.  
- The **NIST Cybersecurity Framework** provides a cycle to manage risks effectively.  

# CyberChef Lab Notes

## 🛠️ Tool Overview: CyberChef
CyberChef is a powerful tool for **encryption, encoding, decoding, and data manipulation**.  

### Four Panels
1. **Input** – Place to enter/paste/upload the data to operate on.  
   - Can add multiple tabs.  
   - Example: typing `100` here.  
2. **Output** – Displays results of operations.  
   - Features: save to file, copy output, replace input.  
   - Magic wand appears if CyberChef suggests relevant operations.  
3. **Operations** – Library of all transformations, grouped by categories.  
   - Example: "From Decimal", "To Hex", "ROT13", "Vigenere".  
4. **Recipe** – The sequence of operations applied to the input.  
   - Drag operations here from the Operations panel.  
   - Supports breakpoints (pause before an operation to inspect progress).  
   - Recipes can be cleared using the Trash icon.  

### Example Conversion
- Input: `100`  
- Recipe: `From Decimal` → `To Hex`  
- Output: `64`  

---

## 👥 Exercise 1: Decode a Simple Cipher
- **Message:** `Terng wbo qrpbqvat lbhe svefg pvcure!`  
- This is a **ROT13** cipher (simple Caesar shift of 13).  
- **Decoded Message:** `Great job decoding your first cipher!`  

✅ Lesson: ROT13 is often used in CTFs and exercises because it’s a symmetric Caesar cipher (applying ROT13 twice returns the original).  

---

## 👥 Exercise 2: Vigenère Cipher with Encoded Key
- **Message:** `Acx'vt dhppu dqpzbui! Yhie im br!`  
- The cipher used here is the **Vigenère Cipher** (a popular polyalphabetic cipher).  
- The **Key** is encoded separately (not polyalphabetic).  
  - First step: determine the encoded key and decode it with a simple method (likely Base64, ROT13, or Hex).  
  - Then use this decoded key to decrypt the Vigenère message.  

✅ Lesson: Some ciphers (like Vigenère) require **both the cipher text and a key**. If the key is obscured with another encoding, you must decode the key first.  

---

## 👥 Exercise 3: Is ROT13 Always a Shift of 13?
- **Message:** `Ijhtinsl rjxxfljx nx kzs, gzy bmfy jqxj hfs bj it?!`  
- This is a **Caesar shift cipher** (ROT-n).  
- ROT13 is one example (shift of 13), but Caesar shifts can be **any number between 1–25**.  
- Use CyberChef’s `ROT13/ROT-n` operation to brute force all possible shifts until readable text appears.  

✅ Lesson: ROT13 is a specific case of Caesar shift. Always check if other shifts are needed.  

---

## 👥 Exercise 4: Broken Image File
- Images are just **binary data**, identified by **Magic Numbers** at the start of the file.  
- If the magic number is incorrect or corrupted, the system won’t recognize the file format.  
- Task: Use CyberChef to fix the magic number in `Lab1_Ex4.png` so the image is viewable.  

✅ Lesson: Magic Numbers (file signatures) are critical for file recognition. For PNG files, the header should start with:  
89 50 4E 47 0D 0A 1A 0A

# Cybersecurity CTFs

### 1. CIA Triad & Security Principles
<img src="https://github.com/user-attachments/assets/accf442f-5972-40ea-82d0-d538260bccbc" width="600">

---

<img src="https://github.com/user-attachments/assets/6fbd3d21-c1c4-48da-b4bc-fcb653b073a7" width="600">

---

<img src="https://github.com/user-attachments/assets/66bc08fe-05e5-42a5-b6bb-ddd210197922" width="600">

---

<img src="https://github.com/user-attachments/assets/e241c1e8-cc11-4732-b53c-c6b160cef4fc" width="600">

---

<img src="https://github.com/user-attachments/assets/9a4fa733-4b2c-4d6a-94f8-b55e93549119" width="600">

---

<img src="https://github.com/user-attachments/assets/8aedf405-a0ba-4c95-bcd1-ba52d9f528e3" width="600">

---

<img src="https://github.com/user-attachments/assets/d395ed73-d216-4b17-8fb3-0b082849d8cc" width="600">


