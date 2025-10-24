
---

````markdown
# 🧠 Linux Part 1 — Basic Command Notes
Practical command references I tested myself on TryHackMe.  
Each command below was verified manually for accuracy and clarity.
````
---

### 🧩 echo
**Command:** `echo`  
Displays text or variables in the terminal.

**Example:**
```bash
echo Hello
````

**Output:**

```
Hello
```

---

### 🧩 whoami

**Command:** `whoami`
Shows the current logged-in user.

**Example:**

```bash
whoami
```

**Output:**

```
tryhackme
```

---

### 🧩 ls

**Command:** `ls`
Lists all folders and files in the current directory.

**Example:**

```bash
ls
```

**Flags:**

* `ls -l` → detailed list (permissions, size, owner)
* `ls -a` → includes hidden files

---

### 🧩 cd

**Command:** `cd`
Moves between directories.

**Examples:**

```bash
cd folder_name     # move into a folder
cd ..              # move back one level
cd ~               # go to home directory
```

---

### 🧩 pwd

**Command:** `pwd`
Displays your exact location (current working directory).

**Example:**

```bash
pwd
```

**Output:**

```
/home/tryhackme/folder4
```

---

### 🧩 cat

**Command:** `cat`
Displays the contents of a file or log.

**Example:**

```bash
cat note.txt
```

---

### 🧩 find -name

**Command:** `find -name`
Finds files or folders by name.

**Examples:**

```bash
find /home -name "note.txt"
find /home -name "*.txt"
```

Use wildcards (`*`) for flexible matching.

---

### 🧩 * (Wildcard)

**Symbol:** `*`
Used to search or match multiple files.

**Example:**

```bash
ls *.txt
```

**Output:**

```
lists all .txt files in the current directory
```

---

### 🧩 grep

**Command:** `grep`
Searches for specific text or patterns inside files.

**Example:**

```bash
grep "192.168.1.1" access.log
```

**Useful flags:**

* `-i` → ignore case
* `-n` → show line numbers
* `-R` → search recursively in directories

---

### 🧩 &

**Symbol:** `&`
Runs a command in the background.

**Example:**

```bash
sleep 60 &
```

This lets you keep using the terminal while the command runs silently in the background.

---

### 🧩 &&

**Symbol:** `&&`
Runs multiple commands — the second executes **only if** the first succeeds.

**Example:**

```bash
mkdir test && cd test
```

---

### 🧩 >

**Symbol:** `>`
Redirects output into a file (overwrites existing content).

**Example:**

```bash
echo hey > welcome.txt
```

**Result:**
Creates `welcome.txt` with “hey” inside.

---

### 🧩 >>

**Symbol:** `>>`
Appends text to a file without overwriting it.

**Example:**

```bash
echo hello >> welcome.txt
```

**Result:**
Adds “hello” below “hey” inside `welcome.txt`.

---

## 🧱 Summary Table

| Command    | Purpose                  | Example                |
| ---------- | ------------------------ | ---------------------- |
| echo       | Display text             | `echo Hello`           |
| whoami     | Show current user        | `whoami`               |
| ls         | List directory contents  | `ls -l`                |
| cd         | Change directory         | `cd folder1`           |
| pwd        | Print current directory  | `pwd`                  |
| cat        | Show file content        | `cat note.txt`         |
| find -name | Find file by name        | `find . -name "*.txt"` |
| grep       | Search text inside files | `grep "error" log.txt` |
| &          | Run in background        | `sleep 60 &`           |
| &&         | Chain commands           | `mkdir x && cd x`      |
| >          | Overwrite file           | `echo A > test.txt`    |
| >>         | Append to file           | `echo B >> test.txt`   |

---

### 🧩 Notes

These are commands I used and tested in **TryHackMe’s Linux Fundamentals Part 1**.
Kept concise, practical, and directly applicable.

```

---



