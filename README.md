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

## 👁 Update Hidden File Permissions

- Modified .project_x.txt to remove write permissions from both user and group, while allowing group read:
'''bash
chmod u-w,g+r,g-w .project_x.txt

## 📂 Restrict Directory Access

-Limited access to the drafts directory so only the researcher2 user can access it:
'''bash
chmod g-x drafts

##📄 Summary

-Established a permissions baseline using:
'''bash
ls -la


-Used the chmod command to bring file and directory permissions in line with access control policies.

-Explained the rationale behind each permission update to ensure transparency and understanding of Linux permission structures.

##📎 Supporting Document

###[📄 File_Permissions_in_Linux.pdf](File_Permissions_in_Linux.pdf)

This PDF includes detailed walkthroughs of each command and justification for the changes made.

🗒️ This lab scenario was part of a hands-on exercise for practicing Linux access control management.
