# 💻 The Complete Windows CMD Commands Guide

[![Windows](https://img.shields.io/badge/Windows-CMD-blue?logo=windows)](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/windows-commands)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

[![by SAMER SAEID ♥️](https://img.shields.io/badge/by-SAMER%20SAEID%20%E2%99%A5%EF%B8%8F-red)](https://bio.link/samer)

## 📖 Description
A **comprehensive reference** for Windows Command Prompt (CMD) commands — from basic navigation and file management to advanced networking, disk utilities, and batch scripting. Perfect for IT professionals, developers, and power users who want to master the Windows command line.

## 🏷️ Tags
`windows` `cmd` `command-line` `batch-scripting` `tutorial` `sysadmin` `terminal` `powershell`

## ✨ Features
- 🔍 **100+ essential CMD commands** explained with syntax and examples
- 📘 **Tutorial‑style** usage for beginners and advanced users
- 🚀 Covers file management, system info, networking, disk operations, and more
- 📂 Organized by categories for quick lookup
- 🎨 **Emojis** next to each command for easy scanning
- 💡 Tips, batch scripting basics, and real‑world examples

---

## 📚 How to Use This Guide
1. Open Command Prompt: press `Win + R`, type `cmd`, and hit Enter.
2. Browse the sections below to find the command you need.
3. Each command includes:
   - 🖍️ **Name** with an emoji
   - 📝 **Description**
   - 💻 **Syntax** and a **practical example**
4. Try the commands in your own CMD window.
5. Use `command /?` to see built‑in help for any command (e.g., `dir /?`).

---

## 📁 File & Directory Management

| Command | Description |
|---------|-------------|
| 📂 `dir` | List directory contents. <br> 💻 `dir` → shows files/folders in current directory. <br> 💻 `dir /w` → wide format. <br> 💻 `dir /s` → include subdirectories. |
| 📂 `cd` | Change directory. <br> 💻 `cd C:\Users` → go to Users folder. <br> 💻 `cd ..` → move up one level. <br> 💻 `cd \` → go to root of current drive. |
| 🧭 `chdir` | Same as `cd`. Also shows current directory if used without arguments. |
| 📁 `mkdir` / `md` | Create a new directory. <br> 💻 `mkdir Projects` → creates folder "Projects". |
| 🗑️ `rmdir` / `rd` | Remove an empty directory. <br> 💻 `rmdir OldFolder` → deletes empty folder. <br> 💻 `rmdir /s OldFolder` → removes folder and all its contents. |
| ❌ `del` / `erase` | Delete one or more files. <br> 💻 `del file.txt` → deletes file. <br> 💻 `del *.tmp` → deletes all .tmp files. <br> 💻 `del /s *.log` → deletes recursively. |
| 📄 `type` | Display contents of a text file. <br> 💻 `type readme.txt` → shows file content. |
| 📋 `copy` | Copy one or more files. <br> 💻 `copy file1.txt file2.txt` → copies file1 to file2. <br> 💻 `copy *.txt D:\Backup\` → copies all .txt files to backup folder. |
| ✂️ `move` | Move or rename files/directories. <br> 💻 `move old.txt new.txt` → renames file. <br> 💻 `move *.txt D:\Docs\` → moves all .txt files. |
| 📝 `ren` / `rename` | Rename a single file or directory. <br> 💻 `ren oldname.txt newname.txt` |
| 🔍 `find` | Search for a text string in files. <br> 💻 `find "ERROR" log.txt` → shows lines containing "ERROR". |
| 🔍 `findstr` | Advanced string search with regex. <br> 💻 `findstr /i "error" *.log` → case‑insensitive search. |
| 🔄 `xcopy` | Advanced copy with options (preserve attributes, copy subdirectories). <br> 💻 `xcopy /s /e source destination` |
| 📂 `robocopy` | Robust file copy (Windows 7+). <br> 💻 `robocopy C:\Source D:\Dest /mir` → mirror copy. |
| 📊 `tree` | Display directory structure graphically. <br> 💻 `tree C:\Projects` → shows folder tree. |

---

## 🖥️ System Information & Management

| Command | Description |
|---------|-------------|
| ℹ️ `systeminfo` | Display detailed system configuration (OS, memory, network, etc.). <br> 💻 `systeminfo` |
| 📊 `tasklist` | List all running processes. <br> 💻 `tasklist` → shows PID, memory usage. <br> 💻 `tasklist /fi "imagename eq chrome.exe"` → filter. |
| ⚡ `taskkill` | Terminate a process by PID or name. <br> 💻 `taskkill /PID 1234 /F` → force kill PID 1234. <br> 💻 `taskkill /IM notepad.exe /F` → kill all Notepad instances. |
| 💾 `wmic` | Windows Management Instrumentation command (powerful queries). <br> 💻 `wmic cpu get name` → CPU info. <br> 💻 `wmic os get caption,version` → OS info. |
| 🔄 `shutdown` | Shutdown, restart, or log off. <br> 💻 `shutdown /s /t 0` → immediate shutdown. <br> 💻 `shutdown /r /t 60` → restart in 60 seconds. <br> 💻 `shutdown /a` → abort pending shutdown. |
| 🔄 `timeout` | Pause for a specified number of seconds. <br> 💻 `timeout /t 5` → wait 5 seconds. |
| ⏲️ `date` / `time` | Display or set system date/time. <br> 💻 `date` → shows current date, prompt to change. <br> 💻 `time /t` → shows time only. |
| 💻 `hostname` | Display computer name. <br> 💻 `hostname` |
| 🔐 `whoami` | Show current user and domain. <br> 💻 `whoami` |
| 📜 `driverquery` | List all installed drivers. <br> 💻 `driverquery /v` → verbose list. |

---

## 🌐 Networking Commands

| Command | Description |
|---------|-------------|
| 🔌 `ipconfig` | Display IP configuration. <br> 💻 `ipconfig` → basic info. <br> 💻 `ipconfig /all` → detailed info (MAC, DNS, etc.). <br> 💻 `ipconfig /release` and `ipconfig /renew` → release/renew DHCP. |
| 🏓 `ping` | Test network connectivity. <br> 💻 `ping google.com` → sends 4 ICMP packets. <br> 💻 `ping -t google.com` → continuous ping (Ctrl+C to stop). |
| 📡 `tracert` | Trace route to a destination. <br> 💻 `tracert google.com` → shows each hop. |
| 🔍 `nslookup` | Query DNS records. <br> 💻 `nslookup google.com` → get IP address. |
| 🗺️ `netstat` | Display network connections and statistics. <br> 💻 `netstat -a` → all connections. <br> 💻 `netstat -b` → show executable (admin rights). <br> 💻 `netstat -ano` → numeric IPs, PIDs. |
| 🔌 `arp` | Display ARP cache. <br> 💻 `arp -a` → list IP‑to‑MAC mappings. |
| 📡 `route` | Display or modify routing table. <br> 💻 `route print` → show routing table. |
| 🔌 `netsh` | Network configuration tool. <br> 💻 `netsh wlan show profiles` → list saved Wi‑Fi networks. <br> 💻 `netsh wlan show profile name=MyWiFi key=clear` → show Wi‑Fi password. |
| 🔍 `getmac` | Display MAC addresses of network adapters. <br> 💻 `getmac` |
| 📡 `telnet` | Connect to remote host via Telnet (optional feature). <br> 💻 `telnet example.com 80` → test port 80. |

---

## 🗜️ Disk & Storage Management

| Command | Description |
|---------|-------------|
| 💾 `chkdsk` | Check disk for errors and bad sectors. <br> 💻 `chkdsk C:` → checks drive C:. <br> 💻 `chkdsk /f C:` → fix errors. <br> 💻 `chkdsk /r` → recover bad sectors. |
| 🔧 `sfc` | System File Checker – repairs corrupted system files. <br> 💻 `sfc /scannow` → scans and repairs. |
| 📀 `diskpart` | Disk partition tool (advanced). <br> 💻 `diskpart` then `list disk` → shows disks. <br> 💻 `select disk 0` then `list partition`. |
| 📊 `wmic diskdrive` | Get disk drive info. <br> 💻 `wmic diskdrive get model,size` |
| 🧹 `cleanmgr` | Launch Disk Cleanup utility. <br> 💻 `cleanmgr` → GUI tool. |
| 🗜️ `compact` | Compress or uncompress files on NTFS. <br> 💻 `compact /c /s:*.*` → compress current folder. |

---

## 🧪 Batch Scripting & Advanced

### 📝 Batch File Basics
- Create a `.bat` or `.cmd` file with any text editor.
- Use `@echo off` to hide commands.
- Use `echo` to output text.
- Use `pause` to wait for user keypress.
- Use `%1`, `%2`, etc. for arguments.

| Command | Description |
|---------|-------------|
| 📢 `echo` | Display message or control echo. <br> 💻 `echo Hello` → prints "Hello". <br> 💻 `echo off` → turn off command echoing. <br> 💻 `@echo off` → prevent echoing of this line. |
| ⏸️ `pause` | Suspends execution and displays "Press any key to continue...". <br> 💻 `pause` |
| 📦 `set` | Set environment variables. <br> 💻 `set myvar=value` → assign. <br> 💻 `echo %myvar%` → use variable. |
| 🔁 `if` | Conditional execution. <br> 💻 `if exist file.txt echo File exists.` <br> 💻 `if "%var%"=="test" (echo True) else (echo False)` |
| 🔂 `for` | Loop over files or values. <br> 💻 `for %i in (*.txt) do echo %i` → list .txt files. <br> 💻 `for /L %%i in (1,1,10) do echo %%i` → count 1–10. |
| 🔄 `goto` | Jump to a label. <br> 💻 `goto :label` → then `:label` in script. |
| 📤 `call` | Call another batch file from within a batch. <br> 💻 `call script2.bat` |
| 🚀 `start` | Launch a program or file. <br> 💻 `start notepad.exe` <br> 💻 `start www.google.com` → open in browser. |
| 🧹 `cls` | Clear the screen. <br> 💻 `cls` |
| 📋 `clip` | Redirect output to clipboard. <br> 💻 `dir | clip` → copies dir listing to clipboard. |
| 🔄 `rem` / `::` | Comment in batch file. <br> 💻 `rem This is a comment` or `:: comment` |

---

## 📘 Tutorials

### 📚 Tutorial 1: Basic Navigation & File Management
```cmd
:: Open CMD
cd \            :: Go to C:\
mkdir MyProject :: Create folder
cd MyProject    :: Enter folder
echo Hello > hello.txt :: Create file with content
type hello.txt  :: View file
copy hello.txt hello_copy.txt :: Copy file
del hello_copy.txt :: Delete copy
cd ..           :: Go back to parent
rmdir MyProject :: Remove folder (must be empty)
