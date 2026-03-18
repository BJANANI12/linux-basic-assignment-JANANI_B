# Linux Basic Assignment

**Name:** Janani B  
**Repo:** linux-basic-assignment-janu

---

## Section 1 – Command Purpose and Example

**1. pwd**  
Shows where you are currently in the file system (current directory path).  
Example: `pwd` → output will be something like `/home/janani`

**2. ls**  
Lists all files and folders in the current directory.  
Example: `ls` → shows files, `ls -l` → shows files with details like size and date

**3. cd**  
Used to move from one folder to another.  
Example: `cd /home/janani/projects` → goes into that folder, `cd ..` → goes back one level

**4. mkdir**  
Creates a new folder.  
Example: `mkdir project-files` → creates a folder called project-files

**5. rm -rf**  
Deletes a file or folder permanently. Be careful — there is no undo!  
Example: `rm -rf old-project` → deletes the old-project folder and everything inside it

**6. ps -ef**  
Shows all the processes currently running on the system with details like process ID and user.  
Example: `ps -ef` → lists all running processes

**7. top**  
Shows real time view of running processes and how much CPU and memory each one is using.  
Example: `top` → opens live monitor, press `q` to quit

**8. df -h**  
Shows how much disk space is used and available on the server in a readable format like GB or MB.  
Example: `df -h` → shows disk usage for all partitions

**9. history**  
Shows a list of all commands you typed before in the terminal.  
Example: `history` → shows last 500 commands with line numbers

**10. uptime**  
Shows how long the server has been running and the current load on the CPU.  
Example: `uptime` → output like `10:30 up 5 days, 2 users, load: 0.10`

---

## Section 2 – Write the Linux Command

**1. Create a directory called project-files**
```
mkdir project-files
```

**2. Navigate into the project-files directory**
```
cd project-files
```

**3. Create a file called notes.txt using vi**
```
vi notes.txt
```
Press `i` to start typing, press `Esc` when done, then type `:wq` and press Enter to save and exit.

**4. Display the contents of notes.txt**
```
cat notes.txt
```

**5. Copy notes.txt to backup.txt**
```
cp notes.txt backup.txt
```

**6. Show the first 100 lines of a file called logs.txt**
```
head -100 logs.txt
```

**7. Show the last 100 lines of logs.txt**
```
tail -100 logs.txt
```

**8. Check the disk storage usage of the server**
```
df -h
```

**9. Check the running processes in the system**
```
ps -ef
```

**10. Delete a file called temp.txt**
```
rm temp.txt
```

---

## Section 3 – Concept Questions

**1. What is the difference between > and >> in Linux?**

`>` overwrites the file completely. If the file has content, it will be replaced.  
`>>` adds to the end of the file without deleting existing content.

Example:
```
echo "Hello" > file.txt    # replaces everything in file.txt
echo "Hello" >> file.txt   # adds Hello to the end of file.txt
```

Note: if the file does not exist, both `>` and `>>` will create it automatically.

---

**2. What is the purpose of the kill -9 command?**

`kill -9` is used to forcefully stop a running process immediately. The -9 sends a SIGKILL signal which the process cannot ignore or block.

First find the process ID using `ps -ef`, then kill it:
```
ps -ef | grep myapp
kill -9 1234
```

---

**3. What is the difference between rm and rmdir?**

`rm` is used to delete files. If you want to delete a folder with files inside, use `rm -rf`.  
`rmdir` only works on empty folders. If the folder has any files inside, it will give an error.

Example:
```
rm temp.txt           # deletes a file
rmdir myfolder        # deletes folder only if it is empty
rm -rf myfolder       # deletes folder even if it has files
```

---

**4. What information does the netstat -tulpn command provide?**

It shows all the open network ports on the server and which service or program is listening on each port.

- t → shows TCP connections
- u → shows UDP connections
- l → shows only listening ports
- p → shows the program name and process ID
- n → shows IP addresses as numbers instead of names

Example use case: check if Spring Boot app is running on port 8080
```
netstat -tulpn | grep 8080
```

---

**5. What is the purpose of the ping command?**

`ping` is used to check if your server can reach another server or website over the network. It sends small packets and waits for a reply.

```
ping google.com
```

If you get replies back → network is working fine  
If you get request timeout → network issue or the server is unreachable

---

## Section 4 – Scenario Based Questions

**1. You want to check the current working directory. Which command will you use?**
```
pwd
```

---

**2. You want to create a directory called devops inside the home directory. Write the command.**
```
mkdir /home/devops
```
Or if you are already inside the home directory:
```
mkdir devops
```

---

**3. You want to check which process is using high CPU in the system. Which command will help?**
```
top
```
Once top is open, press `P` to sort by CPU usage. The process using the most CPU will appear at the top.

---

**4. You want to check whether your server can connect to google.com. Which command will you use?**
```
ping google.com
```

---

**5. You want to view the last 50 lines of a log file called application.log. Write the command.**
```
tail -50 application.log
```

---


