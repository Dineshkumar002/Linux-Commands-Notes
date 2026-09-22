# Basic Commands in Linux

**1. Present working directory:**
```bash
ubuntu@dheen:~$ pwd
/home/ubuntu
```

**2. Version:**
```bash
ubuntu@dheen:~$ uname -a
# version will appear
```

**3. Username:**
```bash
ubuntu@dheen:~$ whoami
ubuntu
```

**4. Clearing the screen:**
```bash
ubuntu@dheen:~$ clear
# Terminal will be cleared (Shortcut: Ctrl + L)
```

**5. Viewing command history:**
```bash
ubuntu@dheen:~$ history
# Total history can be viewed.
```

---

# Creating Directory and Files in Linux

**1. Make directory:**
```bash
ubuntu@dheen:~$ mkdir data
```

**2. Entering into a directory:**
```bash
ubuntu@dheen:~$ cd data/
```

**3. Creating a text file (vi editor):**
```bash
ubuntu@dheen:~/data$ vi hello
```
* **Text file creation steps:**
  * Press `i` to insert text.
  * Enter your text.
  * Press `Esc` to exit insert mode.
  * For saving and quitting: `:wq`
  * Quit without saving: `:q!`

**4. List of files:**
```bash
ubuntu@dheen:~/data$ ls
hello.txt
```

**5. Installing a package:**
```bash
ubuntu@dheen:~/data$ sudo apt-get install vim
# sudo: root user
# apt-get: getting any application
# vim: upgrading vi editor
```

**6. Auto-completing a command:**
Press `Tab` to auto-complete a file name. If multiple files share the same prefix, double-press `Tab` to see options.

**7. Nano Text Editor:**
```bash
ubuntu@dheen:~/data$ nano test.txt
# Nano editor is simple and easy to use.
```

**8. Creating a dummy file:**
```bash
ubuntu@dheen:~/data$ touch foo.txt
```

**9. File manipulation (deleting files):**
```bash
ubuntu@dheen:~/data$ rm foo.txt
ubuntu@dheen:~/data$ ls *.txt
ubuntu@dheen:~/data$ ls he*
ubuntu@dheen:~/data$ rm * # Deletes all files in the current directory
```

---

# Viewing and Copying a File

**1. Displaying content in command prompt:**
```bash
ubuntu@dheen:~/data$ cat hello.txt
This is a file that is created.
```

**2. Copying a file:**
```bash
ubuntu@dheen:~/data$ cp hello.txt new-hello.txt
```

**3. Renaming / Moving a file:**
```bash
ubuntu@dheen:~/data$ mv hello.txt demo.txt
```

**4. Copying a file with 'cat' command (Append symbol `>>`):**
```bash
ubuntu@dheen:~/data$ cat demo.txt >> nfile.txt
# Copies the text from one file to another.
```

**5. Printing texts in prompt:**
```bash
ubuntu@dheen:~/data$ echo "dheen"
dheen
ubuntu@dheen:~/data$ echo "dheen" >> nfile.txt # store in file
ubuntu@dheen:~/data$ echo "mohamed" >> nfile.txt # append in file
```

---

# File Navigation System

**1. Creating nested Directory:**
Use the `-p` flag to create parent directories if they don't exist.
```bash
ubuntu@dheen:~$ mkdir -p abc/test/demo
```

**2. Going Back from a directory:**
```bash
ubuntu@dheen:~/abc/test/demo$ cd ..       # Moves up one level
ubuntu@dheen:~$ cd ../..                  # Moves up two levels
ubuntu@dheen:~$ cd -                      # Goes back to the previous path
ubuntu@dheen:~$ cd ~                      # Navigates to the home directory
```

---

# List Functionalities: (ls)

**1. Basic ls command:**
```bash
ubuntu@dheen:~$ ls
abc data.log print_time.py airflow data hadoop2-din
```

**2. ls options:**

| Option | Description |
| :--- | :--- |
| `-l` | Long list format |
| `-s` | Shows file size in blocks |
| `-t` | Sorts by modification time (newest first) |
| `-r` | Reverses the sorting order |
| `-S` | Sorts by file size (largest first) |

*Example:* `ubuntu@dheen:~$ ls -lstrS`

**3. ls -a (shows hidden files):**
Hidden files start with a dot (`.`). Without `-a`, hidden files are not shown.

| Hidden File / Item | Description |
| :--- | :--- |
| `.bash_history` | Bash command history |
| `.profile` | User profile settings |
| `.bashrc` | Bash configuration file (used for environment variables) |

**4. .bashrc file usage:**
If we install any language (like Python or Java), environment variables are added here.
* Edit: `vi .bashrc`
* Execute changes: `source .bashrc`

**5. Pattern matching with ls:**
```bash
ubuntu@dheen:~$ ls *.py    # Matches files ending in .py
ubuntu@dheen:~$ ls data*   # Matches files starting with 'data'
```

---

# Hardlink and Softlink

**1. Create a file:**
```bash
ubuntu@dheen:~$ echo "hello linux" >> original.txt
```

**2. Hardlink:**
Points to the same data (same inode). Deleting one name does not delete the data. If you update one, the other reflects it.
```bash
ubuntu@dheen:~$ ln original.txt team2-data.txt
```

**3. Softlink (Symbolic link):**
Points to the path of the original file. Deleting the original file breaks the link.
```bash
ubuntu@dheen:~$ ln -s original.txt new-data.txt
```

| Feature | Hardlink | Softlink |
| :--- | :--- | :--- |
| **Inode** | Same inode | Different inode |
| **Link Count** | Increases | No effect |
| **Size** | Same as original | Shows link size only |
| **Cross Filesystem** | Not possible | Possible |
| **Delete Original** | Data stays | Link broken |
| **Type** | File link | Symbolic link |

---

# Background Run & Process Monitor

**1. Running a program in the background:**
```bash
ubuntu@dheen:~$ python3 data.py &
```

**2. nohup command:**
Keeps the process running even after closing the terminal or logging out.
```bash
ubuntu@dheen:~$ nohup python3 data.py >> data.py.log &
```

**3. Process Status and Task Managers:**
* `top`: Displays all running applications live in the task manager.
* `ps`: Shows current running processes.
* `ps -aux`: Gives detailed status of all processes.

**4. Pattern matching processes:**
```bash
ubuntu@dheen:~$ ps -aux | grep data-processing.py
```

**5. Killing a process:**
```bash
ubuntu@dheen:~$ kill -9 <PID> # Sends SIGKILL to stop process immediately
```

**6. Reading Logs live:**
* `tail -f data.py.log`: Follows the file and shows live updates.
* `tail -20 data.py.log`: Shows the last 20 lines once.

---

# Downloading Files & Alias

**1. Downloading (wget):**
Downloads a file from a given URL and saves it in the current directory.
```bash
ubuntu@dheen:~$ wget "https://example.com/linux.jpg"
```

**2. Alias in Linux:**
A shortcut for a long command or path.
```bash
ubuntu@dheen:~$ alias dheen='cd /home/ubuntu/abc/'
```
*Make Alias permanent:*
1. Open file: `vi ~/.bashrc`
2. Add alias at the end of the file.
3. Save and execute: `source ~/.bashrc`

---

# Data - Management

| Command | Description |
| :--- | :--- |
| `df -h` | Shows file-system disk space usage (human-readable format). |
| `du -sh scripts/` | Shows total size of the "scripts/" directory. |
| `free -m` / `free -g` | Shows RAM usage in MB / GB. |
| `sudo sh -c "sync; echo 3>/proc/sys/vm/drop_caches"` | Frees up memory cache (flushes buffers to disk and clears pagecache). |

---

# Zip, Unzip, and TAR Archives

**1. Zip / Unzip:**
* Install: `sudo apt-get install zip`
* Zip a folder recursively: `zip -r file1.zip scripts/`
* Unzip: `unzip file1.zip`

**2. TAR - Archiving and Extracting Files:**
* Create/Compress: `tar -cvzf sample.tar scripts/`
  * `-c`: create archive
  * `-v`: verbose (show files)
  * `-z`: compress (gzip)
  * `-f`: specify archive file name
* Extract: `tar -zxvf sample.tar`
  * `-x`: extract

---

# Word Count, Sort, Head & Tail

**1. Word Count (wc):**
Counts words, characters, and lines.
* `wc file.txt`: Prints lines, words, and characters.
* `wc -w file.txt`: Words only.
* `wc -l file.txt`: Lines only.
* `wc -c file.txt`: Characters only.

**2. Sorting Lines:**
* `sort file.txt`: Sorts alphabetically.
* `sort -n file.txt`: Sorts numerically (ascending order).

**3. Head & Tail Commands:**
* `head file.txt`: Displays first 10 lines.
* `tail file.txt`: Displays last 10 lines.
* `head -n 5 file.txt`: Displays first 5 lines.
* `tail -n 5 file.txt`: Displays last 5 lines.

---

# Pattern Matching & Finding Matches (grep)

Searches for matching patterns within files (case-sensitive by default).

| Command | Output / Explanation |
| :--- | :--- |
| `grep ERROR log2.txt` | Displays lines containing the exact pattern "ERROR". |
| `grep -i error log1.txt` | `-i` makes the search case-insensitive. |
| `grep -v ERROR log1.txt` | `-v` inverts the match (shows lines NOT containing ERROR). |
| `grep WARNING *.txt` | Searches all matching `.txt` files for "WARNING". |
| `grep -r "Timeout" ~/logs` | `-r` searches recursively in directories. |
| `grep "^[ERROR]" log1.txt` | `^` matches the beginning of the line. |

---

# Secure Shell (SSH) & Secure Copy (SCP)

**1. SSH (Connect to a remote server):**
```bash
ubuntu@dheen:~$ sudo apt-get install openssh-server # Install SSH
ubuntu@dheen:~$ ssh ubuntu@192.20.124.118           # Connect via IP
```

**2. SCP (Copy files between servers):**
```bash
# Copy file from local to remote
scp file.txt ubuntu@server:/home/ubuntu/

# Copy directory from local to remote (recursive)
scp -r dir1 ubuntu@server:/home/ubuntu/

# Copy file from remote to local
scp ubuntu@server:/home/ubuntu/file.txt ./
```

---

# FIND COMMAND

Used to locate files by name, size, type, and time at the filesystem level.

| Command | Explanation |
| :--- | :--- |
| `find . -name log1.txt` | Finds files with the exact name. |
| `find . -name "*.txt"` | Finds files ending in `.txt`. |
| `find . -type f -size +10M` | Finds files (`-type f`) strictly larger than 10MB. |
| `find . -mtime -1` | Finds files modified within the last 1 day. |
| `find . -empty` | Finds empty files in the system. |
| `find . -name "*.tmp" -delete`| Locates and immediately deletes `.tmp` files. |

---

# AWK (Command-line Tool)

Used for processing columns in text, performing calculations, and formatting data. By default, columns are separated by spaces or tabs.

* **Print specific columns:**
  ```bash
  awk '{print $1, $3}' data.txt
  ```
* **Filter with conditions:**
  ```bash
  awk '$2 > 27 {print $1, $3}' data.txt
  ```
* **Formatted Output:**
  ```bash
  awk 'printf "Name : %s | Age : %s\n", $1, $2' data.txt
  ```
* **Print specific line ranges using NR (Number of Records):**
  ```bash
  awk 'NR==3, NR==6 {print NR, $0}' employee.txt
  ```

---

# Change Mode (chmod) & Permissions

Controls access files and directories for the **User (u)**, **Group (g)**, and **Others (o)**.

**Permission Values:**
* **Read (r)** = 4
* **Write (w)** = 2
* **Execute (x)** = 1
* **No Permission (-)** = 0

*(Read + Write + Execute = 4 + 2 + 1 = 7)*

**Common numeric permissions:**
| Number | Permission | Meaning |
| :--- | :--- | :--- |
| `777` | `-rwxrwxrwx` | Full access for all. |
| `755` | `-rwxr-xr-x` | Full access to user, read & execute for group & others. |
| `644` | `-rw-r--r--` | Read & write for user, read for group & others. |
| `600` | `-rw-------` | Read & write for user only. |
| `400` | `-r--------` | Read for user only. |

**Examples:**
```bash
ubuntu@dheen:~$ chmod 777 script.sh      # Full access for file
ubuntu@dheen:~$ chmod 755 script.sh      # Standard executable permission
ubuntu@dheen:~$ chmod -R 777 dummy/      # Recursively apply to directory & contents
```
