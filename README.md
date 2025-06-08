# 📁 File Permissions in Linux

This project demonstrates hands-on management of file and directory permissions in a Linux environment. The goal was to align existing permissions with security requirements to ensure proper access control within a fictional organization's `projects` directory.

---

## 🧠 Scenario

Multiple files and directories within the `projects` directory had incorrect permission levels based on organizational policy. I was tasked with auditing these permissions and applying the appropriate changes using the `chmod` command.

---

## ⚙️ Tasks Performed

### ✅ Check File and Directory Details

- Used `ls -la` to list all files (including hidden ones) and inspect current permission settings.

### 🧵 Understand the Permission String

- Explained the components of a file permission string:
  - The first character: `d` for directory or `-` for file
  - Characters 2–4: permissions for user
  - Characters 5–7: permissions for group
  - Characters 8–10: permissions for others

---

## 🔧 Adjust File Permissions

- Removed write permissions for **others** from `project_k.txt`:
  ```bash
  chmod o-w project_k.txt
