#  Linux Part 1 — Basic Command Notes

These are my foundational Linux commands — each tested, verified, and written for fast recall.

---

## 🔹 Echo
**Command:** `echo`
- Displays text or variables in the terminal.
- Example:
  ```bash
  echo Hello
````

→ Prints: `Hello`

---

## 🔹 Whoami

**Command:** `whoami`

* Shows the current logged-in user.
* Example:

  ```bash
  whoami
  ```

  → Output: `tryhackme`

---

## 🔹 ls

**Command:** `ls`

* Lists all folders and files in the current directory.
* Example:

  ```bash
  ls
  ```
* Flags:

  * `ls -l` → detailed list (permissions, size, owner)
  * `ls -a` → includes hidden files

---

## 🔹 cd

**Command:** `cd`

* Moves between directories.
* Examples:

  ```bash
  cd folder_name      # move into a folder
  cd ..               # move back one level
  cd ~                # go to home directory
  ```

---

## 🔹 pwd

**Command:** `pwd`

* Displays your exact location (current working directory).
* Example:

  ```bash
  pwd
  ```

  → `/home/tryhackme/folder4`

---

## 🔹 cat

**Command:** `cat`

* Accesses and displays the contents of a file or log.
* Example:

  ```bash
  cat note.txt
  ```

---

## 🔹 find -name

**Command:** `find -name`

* Finds files or folders by name.
* Example:

  ```bash
  find /home -name "note.txt"
  ```
* Use wildcards (`*`) for flexible matching:

  ```bash
  find /home -name "*.txt"
  ```

---

## 🔹 * (Wildcard)

**Symbol:** `*`

* Used to search or match multiple files.
* Example:

  ```bash
  ls *.txt
  ```

  → Lists all `.txt` files in the current directory.

---

## 🔹 grep

**Command:** `grep`

* Searches for specific text or patterns inside files.
* Example:

  ```bash
  grep "192.168.1.1" access.log
  ```
* Useful flags:

  * `-i` → ignore case
  * `-n` → show line numbers
  * `-R` → search recursively in directories

---

## 🔹 &

**Symbol:** `&`

* Runs a command in the background.
* Example:

  ```bash
  sleep 60 &
  ```

  → Command runs silently while you keep using the terminal.

---

## 🔹 &&

**Symbol:** `&&`

* Runs multiple commands *only if* the first one succeeds.
* Example:

  ```bash
  mkdir test && cd test
  ```

---

## 🔹 >

**Symbol:** `>`

* Redirects output into a file (overwrites existing content).
* Example:

  ```bash
  echo hey > welcome.txt
  ```

  → Creates `welcome.txt` with “hey” inside.

---

## 🔹 >>

**Symbol:** `>>`

* Appends text to a file without overwriting.
* Example:

  ```bash
  echo hello >> welcome.txt
  ```

  → Adds “hello” below “hey” inside `welcome.txt`.

---

###  Summary

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

### 🧠 Notes

These are the commands I actually used and tested in TryHackMe’s Linux Fundamentals Part 1.
Kept short, readable, and practical — no theory, just results.

```


