# CYB101 – Week 3 Notes
---

## Secure Coding & Secure by Design
- **Secure by Design** = building security into every stage of software/system creation (not bolting it on later).
- Cheaper to build securely from the start than to patch later.

### Roles
- **Software Developers (Builders 🧱):**
  - Write secure code
  - Understand common vulnerabilities
- **Cybersecurity Professionals (Blue Team 🛡):**
  - Watch for threats
  - Defend against attacks
  - Detect breaches  

### Practices
- **The Builders 🧱**
  - Input validation → protects against XSS, SQL injection, buffer overflow
  - Secure error handling → prevents info leaks
  - Encrypted data handling → protects against interception & unauthorized access
  - Secure authentication → prevents unauthorized logins & privilege escalation  

- **The Guards 🛡**
  - Continuous monitoring → detect/respond before damage is done
  - Threat intelligence sharing → adapt to real-world attacks
  - Incident response planning → minimize breach impact & recovery time  

---

## Authentication

### Non-Human Identities
- Workloads, services, machines
- Often majority of “users” in organizations
- Usually privileged → larger attack surface
- Static passwords not ideal

### Securing Device Identities
- **Public Key Infrastructure (PKI):** digital certificates for unique IDs
- **On-device code generation:** ensures only authorized access
- **Mutual authentication:** both sides verify each other
- **Zero trust:** no access until verified

### Factors of Authentication
1. **Something you know** (password, PIN)  
   - Weaknesses: easy to forget, reused, guessable, eavesdroppable  
2. **Something you have** (ID card, credit card)  
   - Weaknesses: can be lost or duplicated  
3. **Something you are** (fingerprint, voice, face)  
   - Weaknesses: error rates, similarity between people, cost, privacy concerns  

### Multi-Factor Authentication (MFA)
- Uses 2+ factors together  
- Protects against compromise of a single factor  
- Example:  
  1. Step 1: Login with username/password → “Something you know”  
  2. Step 2: Verification code on device → “Something you have”  

---

## Permissions & Passwords

### Unix File Permissions
- Every file/dir has:
  - Owner & group
  - Permissions for owner, group, and world
- Permissions:
  - **Read (r):** view contents
  - **Write (w):** modify contents
  - **Execute (x):** run file  

- Owner: read, write, execute  
- Group: read, execute  
- World: none  

---

## How Passwords Work
- **Signup:**
  1. Encrypt (hash) user’s password
  2. Store the hash in the database
- **Login:**
  1. User enters password
  2. System hashes input
  3. Compare new hash to stored hash  

### Hashing
- One-way transformation (irreversible)  
- Examples: SHA-2, MD5  

---

## Lab: Password Cracking
- Used brute-force tools against hashed password dumps (e.g., John the Ripper).  
- Discussion:
  - Easy-to-crack passwords = short, common, dictionary words  
  - Harder-to-crack = longer, complex, not in wordlists  

---


