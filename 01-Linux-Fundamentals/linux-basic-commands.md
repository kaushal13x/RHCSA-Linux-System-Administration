# Linux Basic Commands – Beginner to Advanced

**Learning Path:** RHCSA / Linux System Administration  
**Environment:** Linux Virtual Machine using VirtualBox  
**Host OS:** Windows 11  
**Author:** Kaushal Kumar

---

## 1. Introduction to Linux

Linux is an open-source operating system widely used in servers, cloud computing, DevOps, and system administration.

Linux provides a command-line interface (CLI) that allows users to interact with the operating system using commands.

### Why Linux is important?

- Used in cloud platforms like AWS.
- Essential for DevOps and system administration.
- Used in web servers and enterprise infrastructure.
- Supports automation through Shell Scripting.
- Widely used with Docker and Kubernetes.

---

## 2. Basic Linux Commands

### 2.1 `pwd` – Print Working Directory

Displays the current working directory.

**Syntax:**
```bash
pwd
```

**Example:**
```bash
pwd
```

**Output:**
```text
/home/kaushal
```

**Use:** To identify your current location in the Linux filesystem.

### 2.2 `ls` – List Directory Contents

Displays files and directories.

**Examples:**
```bash
ls
ls -l
ls -a
ls -la
```

| Command | Purpose |
|---|---|
| `ls` | Lists files and directories |
| `ls -l` | Detailed listing |
| `ls -a` | Shows hidden files |
| `ls -la` | Detailed listing including hidden files |

### 2.3 `whoami` – Current Username

Displays the username of the currently logged-in user.

```bash
whoami
```

**Example Output:**
```text
kaushal
```

### 2.4 `who` – Logged-in Users

Displays currently logged-in user sessions.

```bash
who
```

### 2.5 `cd` – Change Directory

Used to navigate between directories.

**Examples:**
```bash
cd /home
cd Documents
cd ..
cd ~
cd /
```

| Command | Purpose |
|---|---|
| `cd /home` | Navigate to home parent directory |
| `cd ..` | Move one directory backward |
| `cd ~` | Move to home directory |
| `cd /` | Move to root directory |

---

## 3. File and Directory Management

### 3.1 `mkdir` – Create Directory

Creates a new directory.

```bash
mkdir Linux
mkdir Projects
mkdir -p Linux/RHCSA/Day01
```

### 3.2 `touch` – Create Empty File

Creates a new empty file if it does not exist.

```bash
touch notes.txt
touch commands.md
```

### 3.3 `cp` – Copy Files

Copies files from one location to another.

```bash
cp notes.txt backup.txt
cp notes.txt /tmp/
```

### 3.4 `mv` – Move or Rename Files

Moves files or renames them.

**Rename:**
```bash
mv notes.txt linux-notes.txt
```

**Move:**
```bash
mv linux-notes.txt /tmp/
```

### 3.5 `rm` – Remove Files

Deletes files.

```bash
rm notes.txt
```

**Remove directory recursively:**
```bash
rm -r Linux
```

**Warning:** Be careful while using `rm -r` and especially `rm -rf`, because deleted files may not be recoverable.

---

## 4. Viewing File Contents

### 4.1 `cat` – Display File Content

```bash
cat notes.txt
```

Can also create a file using redirection:

```bash
cat > notes.txt
```

Press `Ctrl + D` to finish entering content.

### 4.2 `head` – Display First Lines

```bash
head notes.txt
head -n 2 notes.txt
```

Displays the first 10 lines by default, or the first 2 lines with `-n 2`.

### 4.3 `tail` – Display Last Lines

```bash
tail notes.txt
tail -n 3 notes.txt
```

Displays the last 10 lines by default, or the last 3 lines with `-n 3`.

---

## 5. Input and Output Redirection

Redirection allows us to save command output into files.

### 5.1 `>` – Overwrite Output

```bash
date > date.txt
```

Saves the date output into `date.txt`. Existing content is overwritten.

### 5.2 `>>` – Append Output

```bash
date >> date.txt
```

Adds the date output at the end of the file without deleting existing content.

### 5.3 `echo` – Display Text

```bash
echo "Hello Linux"
echo "Learning RHCSA" > learning.txt
```

---

## 6. Linux Help Commands

### 6.1 `man` – Manual Pages

Displays the manual of a command.

```bash
man ls
man mkdir
man useradd
```

Press `q` to exit the manual.

### 6.2 `--help` – Command Help

Displays basic usage information.

```bash
ls --help
mkdir --help
cp --help
```

---

## 7. User Management Basics

### 7.1 `useradd` – Create User

Creates a new Linux user.

```bash
sudo useradd testuser
```

### 7.2 `passwd` – Set User Password

```bash
sudo passwd testuser
```

### 7.3 `su` – Switch User

```bash
su - testuser
```

Switches to the specified user.

### 7.4 `exit` – Exit Current Shell

```bash
exit
```

Returns to the previous shell or ends the current shell session.

### 7.5 `logout` – Log Out

```bash
logout
```

Logs out of a login shell.

---

## 8. Process Management

### 8.1 `ps` – Display Processes

```bash
ps
ps aux
```

Displays running processes.

### 8.2 `kill` – Send Signal to Process

```bash
kill PID
```

Sends the default termination signal (SIGTERM) to a process.

Example:
```bash
kill 1234
```

Replace `1234` with the actual process ID.

### 8.3 `Ctrl + C` – Interrupt Process

Stops the currently running foreground command in the terminal by sending an interrupt signal.

---

## 9. Package Management

Package managers help install, update, and remove software.

### 9.1 `rpm`

Used to query, install, and manage RPM packages.

```bash
rpm -qa
rpm -qi package-name
```

### 9.2 `yum`

Package manager used in Red Hat-based Linux distributions.

```bash
sudo yum install httpd
sudo yum update
```

### 9.3 `dnf`

Modern package manager used in current RHEL releases.

```bash
sudo dnf install httpd
sudo dnf update
sudo dnf remove httpd
```

**Note:** DNF and YUM resolve package dependencies automatically. RPM is a lower-level package management tool.

---

## 10. Disk Space Management

### `df -h`

Displays filesystem disk space in a human-readable format.

```bash
df -h
```

Useful for checking available and used disk space.

---

## 11. Vim Editor Basics

Vim is a command-line text editor used to create and edit files.

### Open a file:
```bash
vim notes.txt
```

### Important Vim modes

| Mode | Purpose |
|---|---|
| Normal Mode | Navigate and execute commands |
| Insert Mode | Enter or edit text |
| Command Mode | Save, quit, and execute editor commands |

### Important shortcuts

| Shortcut | Purpose |
|---|---|
| `i` | Enter Insert Mode |
| `Esc` | Return to Normal Mode |
| `:w` | Save file |
| `:q` | Quit |
| `:wq` | Save and quit |
| `:q!` | Quit without saving |
| `dd` | Delete current line |
| `yy` | Copy current line |
| `p` | Paste copied line |

---

## 12. Practical Lab – My First Linux Practice

Try these commands in your Linux Virtual Machine.

### Task 1: Create a directory
```bash
mkdir RHCSA-Practice
```

### Task 2: Enter the directory
```bash
cd RHCSA-Practice
```

### Task 3: Create three files
```bash
touch notes.txt commands.txt practice.txt
```

### Task 4: List files
```bash
ls -l
```

### Task 5: Write content
```bash
echo "I am learning Linux for RHCSA" > notes.txt
```

### Task 6: Display content
```bash
cat notes.txt
```

### Task 7: Create a backup
```bash
cp notes.txt backup.txt
```

### Task 8: Rename a file
```bash
mv practice.txt lab.txt
```

### Task 9: Check current directory
```bash
pwd
```

### Task 10: Check disk space
```bash
df -h
```

---

## 13. What I Learned

After completing these topics, I learned:

- How to navigate the Linux filesystem.
- How to create, copy, move, and delete files.
- How to view and edit file contents.
- How to manage basic Linux users.
- How to check and manage running processes.
- How to understand Linux package managers.
- How to use Vim for text editing.
- How to work with command output and redirection.

---

## 14. My Learning Goal

My goal is to develop strong Linux System Administration skills and prepare for the Red Hat Certified System Administrator (RHCSA) certification.

I will continue documenting my practical experience, commands, troubleshooting steps, and real-world Linux administration labs in this repository.