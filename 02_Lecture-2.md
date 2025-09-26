# CYB101 – Week 2: Encryption 

## Encryption Basics  
- **Encryption**: Converting data into a code  
- Purpose: Prevent unauthorized access, validate integrity, increase density  
- **Decryption**: Extra step attackers must perform  
- **Origins**: Egypt, Greece, Italy, proto-Algonquian speakers  
- **Cipher** = specific process/algorithm  
- **Plaintext passwords** = inexcusable today  

---

## Ciphers  

### Substitution Ciphers  
- Replace characters with symbols, numbers, or letters  
- Examples: **Caesar Cipher, Vernam Cipher, ROT-1**  
- Reversible but insecure  

**Caesar Cipher Example**: Shift letters by 3 → A→D, B→E, etc.  

### Transposition Ciphers  
- Rearrange characters (like an anagram)  
- Example: **Scytale** (ancient cylinder method)  

⚠️ Both substitution and transposition are obsolete → not secure today  

---

## Hashing  

### What is Hashing?  
- Transforms input into fixed-length output  
- **Non-reversible**  
- **Deterministic** → same input, same hash  
- **Brute force resistant** (computationally hard)  

### Common Algorithms  
- MD5, SHA-1, SHA-2, NTLM, LANMAN  

### Password Example  
1. **Account creation**: System stores only the **hash**  
2. **Login**: New password hashed → compared with stored hash  

---

## Key Encryption  

### Encryption Keys  
- Random string of bits  
- **Unique and unpredictable**  
- Scramble/descramble data  

### Symmetric-Key Algorithms  
- One key used for both encryption & decryption  
- Key must be exchanged (**secret key encryption**)  
- Advantage: Faster  
- Disadvantage: Less secure if intercepted  

### Asymmetric-Key Algorithms  
- Uses **key pairs**: one public, one private  
- Public key = shared openly (encrypts messages)  
- Private key = kept secret (decrypts messages)  
- Example: Journalist receiving encrypted messages  
- Advantage: More secure, avoids key sharing risks  
- Disadvantage: Slower  

---

## Secure Sockets Layer (SSL)  

### Overview  
- Protocol for **securing Internet communication**  
- Common in **client-server, email, VoIP**  
- Uses both **symmetric & asymmetric encryption**  

### SSL Certificates  
- Digital document validating a website’s identity  
- Contain server’s public keys  
- Signed by trusted authority  

### TLS/SSL Handshake Steps  
1. **Certificate Verification** – client checks server’s certificate  
2. **Session Key Creation** – client generates symmetric key, encrypts with server’s public key  
3. **Decryption** – server uses private key to decrypt symmetric key  
4. **Secure Communication** – both use symmetric key to exchange data  

---

## AI Checkpoint #1  

**Roles AI can play in learning**:  
- Virtual TA  
- Research helper  
- Debugging partner  
- Clarify terms, explain concepts, brainstorm  

**Best Practices**:  
- ✅ Use AI to check work, brainstorm, clarify  
- ❌ Don’t trust blindly  
- ❌ Don’t copy code without understanding  
- ❌ Don’t replace decision-making  

---
