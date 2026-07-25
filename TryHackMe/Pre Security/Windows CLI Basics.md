# Windows Command Line Basics

## Overview

This module introduced the Windows Command Prompt (CMD) and demonstrated how to interact with the operating system using text-based commands. I learned how to navigate directories, locate files, read file contents, and collect basic system and network information without relying on the graphical user interface (GUI).

---

## Learning Objectives

By completing this module, I was able to:

- Use the Windows Command Line (CMD).
- Navigate folders without using the graphical interface.
- Locate files when only the filename is known.
- Read file contents directly from the terminal.
- Collect basic system and network information.

---

## Commands Learned

### 📂 `cd`

**Purpose:** Change the current directory (navigate between folders).

**Example**
```cmd
cd Documents
```

---

### 📄 `dir`

**Purpose:** Display the contents of the current directory.

**Example**
```cmd
dir
```

*Similar to the `ls` command in Linux.*

---

### 👁️ `dir /a`

**Purpose:** Display all files, including hidden files and folders.

**Example**
```cmd
dir /a
```

---

### 🔍 `dir /s <filename>`

**Purpose:** Search for a file within the current directory and all of its subdirectories.

**Example**
```cmd
dir /s task_brief.txt
```

**Note:** The `/s` flag searches every subfolder and returns the full file path if the file exists.

---

### 📁 `cd <path>`

**Purpose:** Navigate directly to a specific directory.

**Example**
```cmd
cd C:\Users\Parth\Documents
```

Use the `dir` command afterward to verify that the required file exists in the current directory.

---

### 📖 `<filename>`

**Purpose:** Display the contents of a text file directly in the Command Prompt.

**Example**
```cmd
task_brief.txt
```

---

### 👤 `whoami`

**Purpose:** Display the username of the currently logged-in user.

**Example**
```cmd
whoami
```

---

### 💻 `hostname`

**Purpose:** Display the computer's hostname.

**Example**
```cmd
hostname
```

---

### 🖥️ `systeminfo`

**Purpose:** Display detailed information about the operating system and hardware.

**Example**
```cmd
systeminfo
```

Information includes:
- Windows Version
- System Manufacturer
- Processor
- Installed Memory (RAM)
- System Boot Time
- Network Information

---

### 🌐 `ipconfig`

**Purpose:** Display network configuration information.

**Example**
```cmd
ipconfig
```

Information includes:
- IP Address
- Subnet Mask
- Default Gateway
- Network Adapter Details

---

## Key Takeaways

During this module, I learned how to:

- Navigate directories using the command line.
- Search for files without knowing their exact location.
- Display hidden files and folders.
- Read file contents directly from the terminal.
- Identify the currently logged-in user.
- Find the computer's hostname.
- View operating system and hardware information.
- Display network configuration details.

---

## Skills Gained

- Basic Windows Command Prompt navigation.
- File and directory management.
- File searching using command-line tools.
- Reading text files from the terminal.
- Gathering system information.
- Viewing basic network configuration.
- Improved confidence working without a graphical interface.

---

## Practical Applications

The skills learned in this module can be applied to:

- Troubleshooting Windows systems.
- Navigating systems during cybersecurity assessments.
- Finding important files quickly.
- Collecting system information during incident response.
- Identifying network configuration during security investigations.
- Working on remote systems using only the command line.

---

## Reflection

This module introduced the fundamentals of the Windows Command Prompt and demonstrated how powerful the command line can be for managing a system. Learning to navigate directories, search for files, read file contents, and gather system information without relying on the graphical interface is an important skill for IT professionals and cybersecurity analysts.

These command-line skills will serve as a foundation for learning PowerShell, Windows administration, and Security Operations (SOC) workflows.

---

## Status

✅ Completed
