

````markdown
# 🧠 Linux Part 2 — File Management & System Navigation

Practical command references I tested myself on TryHackMe.  
Each command below was verified manually for accuracy and clarity.

---

### 🧩 `ls -a`
**Command:** `ls -a`  
Lists **all files**, including hidden ones (those starting with a `.`).

**Example:**
```bash
ls -a
````

---

### 🧩 `ls --help`

**Command:** `ls --help`
Displays the **manual help page** for `ls`, showing all available options and flags.

**Example:**

```bash
ls --help
```

---

### 🧩 `man ls`

**Command:** `man ls`
Opens the **manual page** for `ls` with detailed explanations and usage examples.

**Example:**

```bash
man ls
```

---

### 🧩 `touch`

**Command:** `touch <filename>`
Creates an **empty file** or updates the timestamp of an existing one.

**Example:**

```bash
touch newnote.txt
```

---

### 🧩 `mkdir`

**Command:** `mkdir <foldername>`
Creates a **new directory (folder)**.

**Example:**

```bash
mkdir myfolder
```

---

### 🧩 `cp`

**Command:** `cp <source> <destination>`
Copies a file or folder to a new location.

**Examples:**

```bash
cp file.txt /home/tryhackme/
cp -r folder1 folder2    # copy directories recursively
```

---

### 🧩 `mv`

**Command:** `mv <source> <destination>`
Moves or **renames** files and directories.

**Examples:**

```bash
mv note.txt myfolder/          # move
mv oldname.txt newname.txt     # rename
```

---

### 🧩 `rm`

**Command:** `rm <filename>`
Deletes a file.

**Example:**

```bash
rm file.txt
```

**Flag:**
`rm -R` → removes directories **recursively** (use with caution).

---

### 🧩 `file`

**Command:** `file <filename>`
Displays the **type of a file**, e.g. ASCII text, directory, binary, etc.

**Example:**

```bash
file unknown1
```

---

### 🧩 `su` & `su -l`

**Command:** `su <username>`
Switches to another user account.

**Command:** `su -l <username>`
Starts a full **login shell** for the target user, inheriting their environment variables.

**Example:**

```bash
su user2
su -l user2
```

---

### 🧩 Key Directories

| Directory | Description                                                |
| --------- | ---------------------------------------------------------- |
| `/etc`    | Contains system-wide **configuration files**.              |
| `/var`    | Stores **variable data** such as logs and temporary files. |
| `/root`   | The **root user’s home directory** (superuser).            |

---

### 🧱 Summary Table

| Command     | Purpose                           | Example              |
| ----------- | --------------------------------- | -------------------- |
| `ls -a`     | List all (including hidden) files | `ls -a`              |
| `ls --help` | Display command help              | `ls --help`          |
| `man ls`    | Open `ls` manual page             | `man ls`             |
| `touch`     | Create new file                   | `touch note.txt`     |
| `mkdir`     | Create directory                  | `mkdir newfolder`    |
| `cp`        | Copy files/folders                | `cp file1 /home/`    |
| `mv`        | Move or rename                    | `mv old.txt new.txt` |
| `rm`        | Remove file                       | `rm file.txt`        |
| `rm -R`     | Remove directory                  | `rm -R folder`       |
| `file`      | Check file type                   | `file unknown1`      |
| `su`        | Switch user                       | `su user2`           |
| `su -l`     | Switch user (login shell)         | `su -l user2`        |
| `/etc`      | Config files directory            | —                    |
| `/var`      | Variable/log data                 | —                    |
| `/root`     | Root home directory               | —                    |

---

🧩 *These notes were built and verified in TryHackMe — Linux Fundamentals Part 2.
Each command was executed and confirmed inside a live environment.*

```




