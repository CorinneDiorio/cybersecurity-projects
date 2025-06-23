# 📂 File Permissions in Linux

## 🔧 Project Overview  
This project involved auditing and modifying file and directory permissions within a Linux environment to enhance system security. Using Linux commands, I identified permission settings, interpreted them, and used `chmod` to enforce the correct authorization levels.

---

## 🪪 Checking File and Directory Details  
Commands used:
```bash
pwd                 # Confirm current directory
cd projects         # Navigate to the target directory
ls -la              # List all files, including hidden, with permissions
```

---

## 🔍 Understanding the Permission String  
Linux file permission strings have 10 characters:

- 1st: File type (`d` for directory, `-` for file)
- 2nd–4th: User permissions (read `r`, write `w`, execute `x`)
- 5th–7th: Group permissions
- 8th–10th: Other (everyone else) permissions

Example: `-rwxr--r--`

---

## ✏️ Modifying File Permissions

### 🚫 Restrict “Other” Write Access
File: `project_k.txt`  
```bash
chmod o-w project_k.txt      # Remove write for others
ls -l project_k.txt          # Verify changes
```

---

### 🙈 Change Hidden File Permissions
File: `.project_x.txt`  
Objective: User and group should have **read-only** access  
```bash
chmod u-w .project_x.txt     # Remove write for user
chmod g-w,+r .project_x.txt  # Remove write, add read for group
```

---

### 📁 Change Directory Access
Directory: `drafts`  
Only `researcher2` should have access  
```bash
chmod g-x drafts             # Remove execute from group
ls -ld drafts                # Verify new permissions
```

---

## 🧾 Summary  
This project reinforced how to:
- Use `ls -la` to audit permissions
- Interpret permission strings
- Apply `chmod` to enforce access control
- Apply principle of least privilege in a real system

---

📁 *End of Report*
