
````markdown
# 🧠 Linux Part 2 — File Management & System Navigation  
Practical command references I tested myself on TryHackMe.  
Each command below was verified manually for accuracy and clarity.

---

### 🧩 ls

**Command:** `ls`  
Lists all files and folders in the current directory.

**Examples:**
```bash
ls
ls -a       # show hidden files
ls --help   # display all available options
```

---

### 🧩 man

**Command:** `man`  
Displays the manual page (documentation) for a command.

**Example:**
```bash
man ls
```

**Tip:**  
Press `q` to exit the manual page.

---

### 🧩 touch

**Command:** `touch`  
Creates an empty file.

**Example:**
```bash
touch file1.txt
```

**Result:**  
Creates a new file named `file1.txt`.

---

### 🧩 mkdir

**Command:** `mkdir`  
Creates a new directory (folder).

**Example:**
```bash
mkdir new_folder
```

---

### 🧩 cp

**Command:** `cp`  
Copies files or directories.

**Examples:**
```bash
cp file1.txt backup.txt          # copy file
cp -r folder1/ backup_folder/    # copy directories recursively
```

---

### 🧩 mv

**Command:** `mv`  
Moves or renames files and directories.

**Examples:**
```bash
mv file1.txt folder1/            # move file
mv oldname.txt newname.txt       # rename file
```

---

### 🧩 rm

**Command:** `rm`  
Removes (deletes) files or directories.

**Examples:**
```bash
rm file1.txt             # remove file
rm -R folder1            # remove directory and its contents
```

⚠️ **Warning:** No recycle bin — deletion is permanent.

---

### 🧩 file

**Command:** `file`  
Determines the type of a file.

**Example:**
```bash
file note.txt
```

**Output Example:**
```
note.txt: ASCII text
```

---

### 🧩 su & su -l

**Commands:** `su`, `su -l`  
Switch users or become the root user.

**Examples:**
```bash
su          # switch to root (current environment)
su -l       # full login shell as root
```

---

### 🧩 /etc

**Directory:** `/etc`  
Contains system-wide configuration files.  
Examples include:
- `/etc/passwd` → user information  
- `/etc/hosts` → local hostname mappings

---

### 🧩 /var

**Directory:** `/var`  
Contains variable data like logs, mail, and temporary files.  
Examples include:
- `/var/log/` → system and application logs  
- `/var/tmp/` → temporary runtime data

---

### 🧩 root

**User/Directory:** `root`  
- The **root user** is the superuser with full control over the system.  
- The **/root directory** is the home folder for that user.

---

## 🧱 Summary Table

| Command | Purpose                        | Example                         |
|----------|--------------------------------|----------------------------------|
| ls       | List files and folders         | `ls -a`                          |
| man      | View command documentation     | `man ls`                         |
| touch    | Create empty file              | `touch file.txt`                 |
| mkdir    | Create directory               | `mkdir new_folder`               |
| cp       | Copy files or directories      | `cp file1 file2`                 |
| mv       | Move or rename files           | `mv file1 folder1/`              |
| rm       | Delete files or directories    | `rm -R folder1`                  |
| file     | Show file type                 | `file note.txt`                  |
| su       | Switch user                    | `su`                             |
| su -l    | Switch to root login shell     | `su -l`                          |
| /etc     | Config files directory         | `/etc/passwd`                    |
| /var     | Logs and variable data         | `/var/log/`                      |
| root     | Superuser / root home folder   | `/root`                          |

---

### 🧩 Notes

These commands were learned and tested during **TryHackMe’s Linux Fundamentals Part 2**.  
Focus: file creation, movement, permissions, and core directories.

