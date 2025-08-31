# Password Cracking with John the Ripper

## 📌 Project Overview
This project explores **password cracking using John the Ripper (JtR)** in a Windows environment.  
A test password hash file (`pass1.txt`) was created, and different cracking modes were tested:

- **Incremental brute-force attack**: Tried all possible combinations (slow).  
- **Dictionary attack**: Used a custom wordlist (`mypass.txt`) and successfully cracked the weak password `secret123` within seconds.

👉 The experiment shows how weak/common passwords can be cracked easily, highlighting the importance of **strong, unique, and complex passwords**.

---

## 🛠️ Technologies & Tools Used
- **John the Ripper (Community Edition 1.9.0-jumbo)** – Main tool for password cracking  
- **Windows 10 Command Prompt** – Environment for execution  
- **Hash File (`pass1.txt`)** – Test password hashes  
- **Custom Wordlist (`mypass.txt`)** – Password guesses for dictionary attack  
- **Text Editor (Notepad)** – Created/edit hash and wordlist files  

---

## ⚙️ System Architecture
1. **Hash Preparation** – Create `pass1.txt` to store password hashes  
2. **Wordlist Creation** – Custom wordlist `mypass.txt` with weak/common passwords  
3. **Run JtR Modes**  
   - Incremental mode (brute force)  
   - Dictionary mode (custom wordlist)  
   - Rule-based hybrid attacks  
4. **Verification of Results** – Using `john --show`  

---

## 🔐 Security Features of JtR
- Supports multiple hash types (MD5, SHA, bcrypt, etc.)  
- Hybrid attacks with rules to mimic real-world cracking  
- Cracked results stored in `.pot` file  
- Benchmarking (`john --test`) to measure performance  
- CPU & GPU acceleration support  
- Helps identify weak passwords to enforce stronger policies  

---

## 🖼️ Example Commands & Outputs

### Dictionary Attack with Custom Wordlist
```bash
john --format=raw-md5 --wordlist=mypass.txt pass1.txt
```

✅ Output:
```
?:secret123
1 password hash cracked, 0 left
```

### Verify Cracked Passwords
```bash
john --show --format=raw-md5 pass1.txt
```
Output:
```
?:secret123
1 password hash cracked, 0 left
```

---

## 📊 Results Table

| Attack Mode               | Cracked Passwords | Time Taken |
|----------------------------|------------------|------------|
| Dictionary (Custom Wordlist) | secret123        | Very Fast  |
| Incremental (Brute Force)  | Attempted (slow) | Long       |
| Rule-based Hybrid          | Modified words   | Moderate   |

---

## 🎯 Learning Outcomes
- Understood how password hashes (MD5) are stored & cracked  
- Learned to use **JtR in multiple modes** (dictionary, brute force)  
- Gained practical skills in creating & using custom wordlists  
- Saw why weak/common passwords are dangerous  
- Realized the importance of **strong password policies**  

---

## ✅ Conclusion
- **John the Ripper** successfully cracked weak passwords.  
- **Dictionary attacks** were fast and effective.  
- **Incremental brute-force** worked but was slow and resource-intensive.  
- The cracked password `secret123` shows the danger of using weak passwords.  

⚠️ This project emphasizes the **need for long, unique, and complex passwords** in real-world systems.

---

## 🔗 Repository
[GitHub Repo](https://github.com/Almase02)
