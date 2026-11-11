# Linux File Deletion Commands

**Learning Path:** RHCSA / Linux System Administration  
**Topic:** File and Directory Management  
**Author:** Kaushal Kumar

---

## 1. Introduction

Linux provides different commands to delete files and directories.

The `rm` command is commonly used for removing files and directories from the Linux filesystem.

**Important:** Linux generally does not provide a recycle bin for files deleted through `rm`. Always verify the target before deleting.

## 2. rm – Remove Files

The `rm` command removes files.

### Syntax

```bash
rm filename
```

### Example

```bash
touch notes.txt
rm notes.txt
```

This creates and then deletes the file.

## 3. rm -f – Forcefully Remove Files

The `-f` option means force.

It removes files without prompting for confirmation and ignores nonexistent files.

### Example

```bash
rm -f oldfile.txt
```

**Use case:** Removing files without interactive confirmation.

## 4. rm -r – Recursive Directory Removal

The `-r` option means recursive.

It removes a directory along with its contents.

### Example

```bash
mkdir test-folder
touch test-folder/file1.txt
rm -r test-folder
```

The directory and its contents are removed.

## 5. rm -rf – Recursive and Forceful Removal

Combines recursive and force options.

### Example

```bash
mkdir test-folder
touch test-folder/file1.txt
rm -rf test-folder
```

It removes the directory and its contents without prompting.

**Warning:** This command can permanently delete important data. Never use it on system directories or paths you have not verified.

## 6. Difference Between rm Commands

| Command | Purpose |
|---|---|
| `rm file.txt` | Remove a file |
| `rm -f file.txt` | Forcefully remove a file |
| `rm -r folder` | Remove a directory recursively |
| `rm -rf folder` | Forcefully remove a directory recursively |

## 7. Practical Lab

Perform these tasks in your Linux Virtual Machine.

### Task 1: Create a directory

```bash
mkdir deletion-lab
```

### Task 2: Enter the directory

```bash
cd deletion-lab
```

### Task 3: Create files

```bash
touch file1.txt file2.txt file3.txt
```

### Task 4: List files

```bash
ls -l
```

### Task 5: Remove one file

```bash
rm file1.txt
```

### Task 6: Remove a directory recursively

First return to the parent directory:

```bash
cd ..
```

Then remove the lab directory:

```bash
rm -r deletion-lab
```

## 8. What I Learned

- How to remove files using `rm`.
- How to use the force option `-f`.
- How recursive directory deletion works.
- Difference between `rm`, `rm -f`, `rm -r` and `rm -rf`.
- Why safe file deletion practices are important.

## 9. Learning Goal

My goal is to understand Linux file management and safely perform file and directory operations as part of my RHCSA preparation.
