

````markdown
# 🧠 Linux Part 3 — Linux Essentials — Process, Networking, and Automation
Practical command references I tested myself on TryHackMe.  
Each command below was verified manually for accuracy and clarity.
````

---

### 🧩 nano

**Command:** `nano`
Lightweight terminal text editor. Use `Ctrl` + key combos shown at the bottom (e.g., `Ctrl+O` to save, `Ctrl+X` to exit).

**Example:**

```bash
nano note.txt
```

**Controls (common):**

* `Ctrl+O` → write out (save)
* `Ctrl+X` → exit
* `Ctrl+K` → cut line
* `Ctrl+U` → paste

---

### 🧩 vim

**Command:** `vim`
Powerful, configurable editor available on almost every Unix system. Modal (normal/insert/visual) and highly customizable with configs and plugins. Good when `nano` isn't available.

**Example:**

```bash
vim note.txt
```

**Quick cheatsheet:**

* `i` → enter insert mode
* `Esc` → return to normal mode
* `:w` → save
* `:q` → quit
* `:wq` → save and quit
* `dd` → delete line
* `yy` → copy (yank) line
* `p` → paste

---

### 🧩 wget

**Command:** `wget`
Download files from the web when you know the exact URL.

**Example:**

```bash
wget https://example.com/file.zip
```

---

### 🧩 scp

**Command:** `scp`
Secure copy over SSH — transfer files to/from remote machines.

**Copy local → remote:**

```bash
scp file.ext username@IP:/home/username/file.ext
```

**Copy remote → local:**

```bash
scp username@IP:/home/username/file.ext file.ext
```

---

### 🧩 Python3 -m http.server

**Command:** `python3 -m http.server`
Quick static HTTP server to serve files from current directory. Useful for transferring files to a remote machine with `wget` or a browser.

**Example:**

```bash
python3 -m http.server 8000
# on remote: wget http://LOCAL_IP:8000/filename
```

**Note:** directory and filename must be exact or you’ll get 404.

---

### 🧩 ps / ps aux

**Command:** `ps` / `ps aux`
View running processes. `ps` shows current shell processes; `ps aux` shows all processes from all users.

**Examples:**

```bash
ps
ps aux | grep ssh
```

---

### 🧩 top

**Command:** `top`
Interactive view of running processes, CPU/memory usage, and real-time stats.

**Example:**

```bash
top
```

---

### 🧩 kill

**Command:** `kill`
Send signals to processes by PID. Common signals: `SIGTERM` (15), `SIGKILL` (9), `SIGSTOP` (19).

**Example:**

```bash
kill 1234           # SIGTERM by default
kill -9 1234        # SIGKILL (force)
kill -SIGSTOP 1234  # pause process
```

**Note:** `SIGTERM` allows graceful cleanup; `SIGKILL` forces termination.

---

### 🧩 systemctl

**Command:** `systemctl`
Manage systemd services (start/stop/enable/disable).

**Examples:**

```bash
sudo systemctl start apache2
sudo systemctl stop apache2
sudo systemctl enable apache2   # start on boot
sudo systemctl disable apache2  # do not start on boot
```

---

### 🧩 Ctrl+Z / fg

**Symbol:** `Ctrl+Z` / `fg`
`Ctrl+Z` suspends (pauses) the foreground job and sends it to background as stopped. Use `fg` to bring it back to foreground.

**Example:**

```bash
# while a process is running in foreground:
Ctrl+Z
# list jobs
jobs
# bring job 1 back
fg %1
```

---

### 🧩 crontab -e / crontab -l

**Command:** `crontab -e` / `crontab -l`
Edit (`-e`) or list (`-l`) cron jobs for the current user. Cron schedule fields: `m h dom mon dow command`.

**Example entry:**

```cron
0 5 * * 1 tar -zcf /var/backups/home.tgz /home/
```

**Fields meaning:**

* `m` → Minute (0–59)
* `h` → Hour (0–23)
* `dom` → Day of month (1–31)
* `mon` → Month (1–12)
* `dow` → Day of week (0–7, Sun=0 or 7)
* Use `*` for any value.
  **Special:** `@reboot` runs the job at boot.

---

### 🧩 add-apt-repository

**Command:** `add-apt-repository`
Add an APT repository to the system so you can install packages from that source.

**Example:**

```bash
sudo add-apt-repository ppa:some/ppa
sudo apt update
```

---

### 🧩 apt / dpkg / gpg

**Commands:** `apt`, `dpkg`, `gpg`

* `apt` → high-level package manager (install, update, remove).
* `dpkg` → low-level Debian package installer (`.deb` files).
* `gpg` → verify package/signature integrity and trust.

**Examples:**

```bash
sudo apt update
sudo apt install package-name
sudo dpkg -i package.deb
gpg --verify package.sig package.tar.gz
```

---

### 🧩 /var/log

**Path:** `/var/log`
Primary location for system logs — authentication attempts, service errors, and other system events.

**Examples:**

```bash
ls /var/log
sudo tail -f /var/log/auth.log
sudo tail -f /var/log/syslog
```

---

## 🧱 Summary Table

| Command / Topic             | Purpose / Quick note                                | Example                                           |           |
| --------------------------- | --------------------------------------------------- | ------------------------------------------------- | --------- |
| `nano`                      | Lightweight terminal editor                         | `nano note.txt`                                   |           |
| `vim`                       | Powerful modal editor, available widely             | `vim note.txt`                                    |           |
| `wget`                      | Download file by URL                                | `wget https://example.com/file.zip`               |           |
| `scp`                       | Secure copy over SSH (local ↔ remote)               | `scp file user@IP:/home/user/file`                |           |
| `python3 -m http.server`    | Quick file server for transfers                     | `python3 -m http.server 8000`                     |           |
| `ps` / `ps aux`             | List processes                                      | `ps aux                                           | grep ssh` |
| `top`                       | Interactive process viewer                          | `top`                                             |           |
| `kill`                      | Terminate or signal processes                       | `kill -9 PID`                                     |           |
| `systemctl`                 | Manage services and boot enable/disable             | `sudo systemctl enable apache2`                   |           |
| `Ctrl+Z` / `fg`             | Suspend foreground job / resume foreground          | `Ctrl+Z` then `fg %1`                             |           |
| `crontab -e` / `crontab -l` | Schedule recurring jobs (m h dom mon dow)           | `0 5 * * 1 tar -zcf /var/backups/home.tgz /home/` |           |
| `add-apt-repository`        | Add package repositories                            | `sudo add-apt-repository ppa:some/ppa`            |           |
| `apt` / `dpkg` / `gpg`      | Package management and integrity verification       | `sudo apt install pkg` / `sudo dpkg -i file.deb`  |           |
| `/var/log`                  | System and auth logs — check here for events/errors | `sudo tail -f /var/log/auth.log`                  |           |

---

### 🧩 Notes

These are commands and tips I used and tested in TryHackMe’s Linux fundamentals. Kept concise, practical, and directly applicable.
