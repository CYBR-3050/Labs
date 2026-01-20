# CYBR 3050 – Lab 1: Linux Fundamentals for Cyber Operations

## Background
This lab introduces foundational Linux skills that are essential for cyber operations and defense. 
You will work in a Kali Linux virtual machine and practice navigating the filesystem, learning new 
tools using manual pages, managing users, and analyzing files using common Linux utilities.

All tasks in this lab align with real-world defensive and operational scenarios where analysts must 
quickly locate files, review configuration changes, and manage system access.

---

## Step 1: Cloning the Lab Repository from GitHub

The files needed for this lab are stored in a GitHub repository. Begin by cloning the repository 
to your Kali Linux virtual machine.

1. Open a terminal.
2. Navigate to a directory where you store lab work (for example, your home directory).
3. Clone the repository:
   ```bash
   git clone https://github.com/CYBR-3050/Lab1
   ```
4. Change into the cloned directory:
   ```bash
   cd Lab1
   ```

Verify that you see a `content/` directory.

### Reflection Questions
- Why is using a version control system like Git useful in cybersecurity operations?
- What risks might exist if sensitive configuration files are stored in a public repository?

---

## Step 2: Navigating the Linux File System

Practice moving through the Linux filesystem and identifying important directories.

1. Display your current directory:
   ```bash
   pwd
   ```
2. List the contents of the current directory:
   ```bash
   ls
   ```
3. Navigate to the root directory and list its contents:
   ```bash
   cd /
   ls
   ```
4. Return to your home directory:
   ```bash
   cd ~
   ```

### Reflection Questions
- What is the purpose of the `/home` directory?
- Why is it important for cybersecurity professionals to understand the filesystem hierarchy?

---

## Step 3: Using Man Pages to Learn Linux Tools

Linux provides built-in documentation for most commands using manual (man) pages.

1. View the manual page for the `ls` command:
   ```bash
   man ls
   ```
2. Find an option that changes how files are displayed.
3. Exit the manual page.

Repeat this process for:
- `grep`
- `diff`
- `useradd`

### Reflection Questions
- How can man pages help you safely use unfamiliar tools?
- Why is relying on official documentation important in security-sensitive environments?

---

## Step 4: Adding and Managing Users

User management is a core defensive task.

1. Create a new user:
   ```bash
   sudo useradd labuser
   ```
2. Set a password for the new user:
   ```bash
   sudo passwd labuser
   ```
3. Switch to the new user:
   ```bash
   su labuser
   ```
4. Confirm your current user:
   ```bash
   whoami
   ```
5. Return to your original account.

### Reflection Questions
- Why should daily tasks not be performed as the root user?
- How does improper user management increase attack surface?

---

## Step 5: Searching Files with Grep

Security analysts often search logs for indicators of compromise.

1. Navigate to the logs directory:
   ```bash
   cd materials/logs
   ```
2. List the log files.
3. Search all log files for the word "password":
   ```bash
   grep password *
   ```

### Reflection Questions
- Why are keywords like "password" important during log analysis?
- What challenges might arise when searching very large log datasets?

---

## Step 6: Identifying Configuration Changes with Diff

Detecting configuration changes is critical for system integrity.

1. Navigate to the configs directory:
   ```bash
   cd ../configs
   ```
2. Compare the two configuration files:
   ```bash
   diff app.conf.v1 app.conf.v2
   ```

### Reflection Questions
- What change was made between the two configuration files?
- How could unauthorized configuration changes impact system security?

---

## Step 7: Lab Completion
Ensure you have answered all reflection questions in a single document. 
This document will be submitted for lab credit.

Read through chapters 1 & 2 of [**Linux Basics for Hackers**](https://learning.oreilly.com/library/view/linux-basics-for/9798341655102/xhtml/ch01.xhtml)

Discuss one new skill you tried beyond the commands detailed in this document. 

### Final Reflection
- Which Linux skill from this lab do you think will be most useful in later cybersecurity labs?
