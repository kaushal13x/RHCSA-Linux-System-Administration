i# Linux Command History

**Learning Path:** RHCSA / Linux System Administration  
**Topic:** Linux Fundamentals  
**Author:** Kaushal Kumar

---

## 1. Introduction

The `history` command is used to display previously executed commands in the Linux terminal.

It helps users review their command activity and repeat previously executed commands.

## 2. Basic History Command

### Syntax

```bash
history
```

Displays the list of previously executed commands with their history numbers.

### Example

```bash
history
```

Example Output:

```text
1  pwd
2  ls
3  mkdir Linux
4  cd Linux
5  touch notes.txt
6  whoami
```

*Note: Output depends on your actual command history.*

## 3. Display Last Commands

To display the last 5 commands:

```bash
history 5
```

To display the last 10 commands:

```bash
history 10
```

## 4. Execute Previous Commands

### 4.1 Execute the Last Command

```bash
!!
```

Repeats the previously executed command.

### 4.2 Execute a Command by History Number

```bash
!3
```

Executes the command numbered 3 in the history list.

**Important:** Check the command before executing it, especially if it contains deletion or administrative operations.

## 5. Search Command History

### 5.1 Search Using Ctrl + R

Press:

```text
Ctrl + R
```

Then type a keyword to search previously used commands.

Press Enter to execute the selected command.

Press Ctrl + R again to search older matches.

Press Ctrl + C to cancel the search.

## 6. History File

In Bash, command history is generally stored in:

```bash
~/.bash_history
```

To view the file:

```bash
cat ~/.bash_history
```

The history file usually stores commands from previous shell sessions. Current session commands may be written when the shell exits, depending on its configuration.

## 7. Useful History Settings

### HISTSIZE

Controls the number of commands kept in the current shell's history list.

```bash
echo $HISTSIZE
```

### HISTFILE

Displays the file used to save Bash command history.

```bash
echo $HISTFILE
```

## 8. Clear Command History

```bash
history -c
```

Clears the current shell's in-memory history list.

**Warning:** Do not use history-clearing commands just for practice. They can remove useful troubleshooting records.

## 9. Practical Lab

Perform these tasks in your Linux Virtual Machine:

1. Execute `pwd`.
2. Execute `ls`.
3. Execute `whoami`.
4. Execute `date`.
5. Display command history using `history`.
6. Display the last 5 commands using `history 5`.
7. Repeat the last command using `!!`.
8. Search for a previous command using `Ctrl + R`.
9. Check the history file location using `echo $HISTFILE`.
10. View saved history using `cat ~/.bash_history`.

## 10. What I Learned

- How to view previously executed commands.
- How to display a limited command history.
- How to repeat previous commands.
- How to search commands using Ctrl + R.
- Where Bash stores command history.
- How to check HISTSIZE and HISTFILE.

## 11. Learning Goal

My goal is to become comfortable with Linux command-line operations and use command history efficiently during system administration and troubleshooting.
