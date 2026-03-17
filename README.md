#  🐧 Linux Basic Assignment - JANANI B

> **Student:** Janani B | **College:** New Prince Shri Bhavani College of Engineering and Technology
> **Program:** Full Stack Development | **Repo:** `linux-basic-assignment-janani B`

---

## 📋 Table of Contents
- [Section 1 – Command Purpose & Examples](#section-1--command-purpose--examples)
- [Section 2 – Linux Commands for Tasks](#section-2--linux-commands-for-tasks)
- [Section 3 – Concept Questions](#section-3--concept-questions)
- [Section 4 – Scenario Based Questions](#section-4--scenario-based-questions)

---

## 📌 Section 1 – Command Purpose & Examples

| # | Command | Purpose | Example |
|---|---------|---------|---------|
| 1 | `pwd` | Print Working Directory — shows current location in file system | `pwd` → `/home/janu` |
| 2 | `ls` | List all files and folders in the current directory | `ls` → files list \| `ls -l` → detailed |
| 3 | `cd` | Change Directory — navigate into a folder | `cd /home/janu/projects` \| `cd ..` → go back |
| 4 | `mkdir` | Make Directory — creates a new folder | `mkdir project-files` |
| 5 | `rm -rf` | Remove files/folders forcefully & recursively ⚠️ permanent | `rm -rf old-project` |
| 6 | `ps -ef` | Shows all running processes with full details (PID, user, command) | `ps -ef` |
| 7 | `top` | Real-time display of processes, CPU & memory usage | `top` → press `q` to quit |
| 8 | `df -h` | Disk Free — shows disk storage usage in human-readable format | `df -h` → used/free per partition |
| 9 | `history` | Shows list of all previously typed commands in terminal | `history` → last 500 commands |
| 10 | `uptime` | Shows how long server has been running + CPU load average | `uptime` → `up 5 days, load: 0.10` |

---

## 📌 Section 2 – Linux Commands for Tasks

**1. Create a directory called `project-files`**
```bash
mkdir project-files
```

**2. Navigate into the `project-files` directory**
```bash
cd project-files
```

**3. Create a file called `notes.txt` using vi**
```bash
vi notes.txt
```
> Press `i` → type content → press `Esc` → type `:wq` → press `Enter` to save and exit.

**4. Display the contents of `notes.txt`**
```bash
cat notes.txt
```

**5. Copy `notes.txt` to `backup.txt`**
```bash
cp notes.txt backup.txt
```

**6. Show the first 100 lines of `logs.txt`**
```bash
head -100 logs.txt
```

**7. Show the last 100 lines of `logs.txt`**
```bash
tail -100 logs.txt
```

**8. Check the disk storage usage of the server**
```bash
df -h
```

**9. Check the running processes in the system**
```bash
ps -ef
```

**10. Delete a file called `temp.txt`**
```bash
rm temp.txt
```

---

## 📌 Section 3 – Concept Questions

### Q1. What is the difference between `>` and `>>` in Linux?

| Symbol | Meaning | Example |
|--------|---------|---------|
| `>` | **Overwrites** the file completely | `echo "Hello" > file.txt` → replaces all content |
| `>>` | **Appends** to the end of the file | `echo "Hello" >> file.txt` → adds to end |

> 💡 **Note:** If the file does not exist, both `>` and `>>` will **create** it automatically.

---

### Q2. What is the purpose of the `kill -9` command?

- `kill -9 <PID>` **forcefully terminates** a process immediately.
- `-9` is the **SIGKILL** signal — the process **cannot ignore** or block it.
- First use `ps -ef` to find the PID, then kill it:

```bash
ps -ef | grep myapp     # find the PID
kill -9 1234            # forcefully kill it
```

---

### Q3. What is the difference between `rm` and `rmdir`?

| Command | Use | Example |
|---------|-----|---------|
| `rm` | Deletes **files**. Use `rm -rf` for folders with content | `rm temp.txt` \| `rm -rf myfolder` |
| `rmdir` | Deletes **only empty** directories. Fails if folder has files | `rmdir myfolder` *(only if empty)* |

---

### Q4. What information does `netstat -tulpn` provide?

Shows all **open network ports** and the **services listening** on them.

| Flag | Meaning |
|------|---------|
| `t` | TCP connections |
| `u` | UDP connections |
| `l` | Listening ports only |
| `p` | Process name and PID |
| `n` | IP addresses as numbers (not hostnames) |

```bash
netstat -tulpn | grep 8080    # check if Spring Boot is running on port 8080
```

---

### Q5. What is the purpose of the `ping` command?

- Tests **network connectivity** between your system and another host.
- Sends **ICMP packets** and waits for a reply.

```bash
ping google.com
```

- ✅ **Replies received** → Network is working
- ❌ **Request timeout** → Network issue or host unreachable

---

## 📌 Section 4 – Scenario Based Questions

### Q1. Check the current working directory
```bash
pwd
```

---

### Q2. Create a directory called `devops` inside the home directory
```bash
mkdir /home/devops
```
> Or if you are already inside the home directory:
```bash
mkdir devops
```

---

### Q3. Check which process is using high CPU
```bash
top
```
> `top` shows real-time CPU & memory usage. Press `P` to sort by CPU usage — highest CPU process appears at the top.

---

### Q4. Check whether your server can connect to `google.com`
```bash
ping google.com
```

---

### Q5. View the last 50 lines of `application.log`
```bash
tail -50 application.log
```

---

## ✅ Submission Info

- **GitHub Repo:** `linux-basic-assignment-janani B`
- **Visibility:** Public
- **All sections completed:** Section 1 ✅ | Section 2 ✅ | Section 3 ✅ | Section 4 ✅


