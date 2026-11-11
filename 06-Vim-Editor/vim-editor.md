# Vim Editor – Complete Beginner Notes`

**Learning Path:** RHCSA / Linux System Administration  
**Environment:** Red Hat Enterprise Linux / Linux VM  
**Author:** Kaushal Kumar

---

## 1. Introduction to Vim

Vim is a powerful command-line text editor used in Linux to create, edit, and modify files.

It is widely used by Linux administrators and DevOps engineers because it works directly inside the terminal.

### Why Vim is important?

- Used to edit Linux configuration files.
- Useful for remote server administration through SSH.
- Helps edit scripts and configuration files.
- Available on many Linux distributions.

## 2. Open or Create a File

Syntax:

```bash
vim filename
```

Example:

```bash
vim index.html
vim notes.txt
```

If the file does not exist, Vim opens a new buffer and creates the file when you save it.

## 3. Vim Modes

Vim has three commonly used modes.

### 3.1 Normal Mode

- Default mode when Vim opens.
- Used for navigation and editing commands.
- Press `Esc` to return to Normal Mode.

### 3.2 Insert Mode

- Used to write or modify text.
- Press `i` to enter Insert Mode.
- Press `Esc` to return to Normal Mode.

### 3.3 Command-Line Mode

- Used to save and quit files.
- Press `:` in Normal Mode to enter this mode.

Example:

```vim
:w
:q
:wq
```

## 4. Important Vim Commands

| Command | Description |
|---|---|
| `i` | Enter Insert Mode before cursor |
| `a` | Enter Insert Mode after cursor |
| `o` | Open a new line below |
| `Esc` | Return to Normal Mode |
| `:w` | Save file |
| `:q` | Quit Vim |
| `:wq` | Save and quit |
| `:q!` | Quit without saving changes |
| `:w filename` | Save using another filename |

## 5. Cursor Navigation

Vim provides keyboard shortcuts to navigate without a mouse.

| Key | Description |
|---|---|
| `h` | Move left |
| `j` | Move down |
| `k` | Move up |
| `l` | Move right |
| `w` | Move to next word |
| `b` | Move to previous word |
| `e` | Move to end of word |
| `0` | Move to beginning of line |
| `$` | Move to end of line |
| `gg` | Move to first line |
| `G` | Move to last line |

## 6. Copy, Delete and Paste

| Command | Description |
|---|---|
| `yy` | Copy current line |
| `p` | Paste after cursor |
| `P` | Paste before cursor |
| `dd` | Delete current line |
| `dw` | Delete a word |
| `x` | Delete character under cursor |
| `u` | Undo last change |
| `Ctrl + r` | Redo last undone change |

## 7. Searching in Vim

Search for a word:

```vim
/Linux
```

Search for the next occurrence:

```vim
n
```

Search for the previous occurrence:

```vim
N
```

## 8. Useful Vim Commands

Delete all lines:

```vim
:%d
```

Go to a specific line:

```vim
:10
```

Show line numbers:

```vim
:set number
```

Hide line numbers:

```vim
:set nonumber
```

## 9. Practical Examples

### Example 1: Create a file

```bash
vim linux-notes.txt
```

Press `i` and type:

```text
I am learning Linux.
I am preparing for RHCSA.
```

Press `Esc`, then type:

```vim
:wq
```

### Example 2: Open and edit an existing file

```bash
vim linux-notes.txt
```

Press `i`, make changes, then:

```vim
:wq
```

### Example 3: Quit without saving

Open a file, make a change, press `Esc`, then:

```vim
:q!
```

The unsaved changes will be discarded.

## 10. Practical Lab – Vim Editor

Complete these tasks in your Linux Virtual Machine:

1. Create a file named `practice.txt`.
2. Write five lines using Insert Mode.
3. Save the file using `:w`.
4. Navigate using `h`, `j`, `k`, and `l`.
5. Copy a line using `yy`.
6. Paste the line using `p`.
7. Delete a line using `dd`.
8. Search for a word using `/word`.
9. Display line numbers using `:set number`.
10. Save and quit using `:wq`.

## 11. What I Learned

- How to open and create files using Vim.
- Difference between Normal, Insert and Command-Line modes.
- How to navigate through files.
- How to copy, delete and paste text.
- How to search for words.
- How to save and exit files.
- How Vim helps in Linux administration.

## 12. Learning Goal

My goal is to become comfortable with Vim for editing Linux configuration files, scripts and system administration tasks as part of my RHCSA preparation.
