<table>
<tr>
<td><img src="app.ico" width="48" alt="App Icon"></td>
<td>

# Bookmark Backup Tool Professional

</td>
</tr>
</table>


[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE.txt)
[![.NET 8](https://img.shields.io/badge/.NET-8.0-purple.svg)]()
[![Windows 10/11](https://img.shields.io/badge/Platform-Windows%2010%2F11-blue.svg)]()
[![Release](https://img.shields.io/badge/Release-v2.3.0-green.svg)]()
[![CLI Parity](https://img.shields.io/badge/CLI-100%25%20Parity-brightgreen.svg)]()
[![Self-Contained](https://img.shields.io/badge/Dependencies-None-orange.svg)]()

---

# 🎯 Editions

## 🟦 Full Edition (Professional)
- ✓ Complete bookmark management  
- ✓ Intelligent import (auto-detect browser from file extension + naming)  
- ✓ Smart file filtering  
- ✓ **Automated scheduling (Daily/Weekly/Monthly)**  
- ✓ 100% CLI parity  
- ✓ Enterprise logging + task management  
- ✓ PATH integration  
- Size: ~101MB (~32.8MB installer)

## 🟩 Lite Edition
- ✓ Same powerful import/export engine  
- ✓ CLI parity (minus scheduler)  
- ✓ Intelligent import / smart file filtering  
- ❌ Scheduler not included  
- Size: ~101MB (~32.7MB installer)

### 🚨 CLI Naming (Unified)
Regardless of edition installed, the CLI entry point is ALWAYS:

```
BookmarkBackupTool.exe
```

Edition differences are enforced internally.

---

# 🚀 Professional Installers

| Installer Type | Full Edition | Lite Edition | Use Case |
|----------------|--------------|--------------|----------|
| **EXE (Inno Setup)** | BookmarkBackupTool-Full-Setup.exe | BookmarkBackupTool-Lite-Setup.exe | Standard users |
| **MSI (Enterprise)** | BookmarkBackupTool-Full-v2.3.0.msi | BookmarkBackupTool-Lite-v2.3.0.msi | Group Policy, SCCM |

### Installer Features
- Self-contained runtime (no .NET required)  
- Adds **BookmarkBackupTool.exe** to PATH  
- Start Menu entries  
- Uninstall cleans PATH  
- Professional branding  

---

# 🆕 What’s New in v2.3.0 (Dec 2025)

## ⭐ Dual-Format Export System
**Exports both native format AND HTML by default**
- Chrome/Edge → JSON + HTML  
- Firefox → SQLite + HTML  

Optional HTML-only mode:
- GUI: checkbox  
- CLI: `--html`

## ⭐ Smart Browser Detection & Auto-Close
- Detects running Chrome, Edge, Firefox  
- Warns user (GUI) or prompts (CLI)  
- Offers to close browsers automatically  
- Graceful shutdown:  
  1. `CloseMainWindow()`  
  2. Wait 3s  
  3. Force kill if needed  
- Then retries import automatically

## ⭐ UI & Workflow Improvements
- Larger window (height 850px)  
- Activity log (fixed height + scrollable)  
- Export options in a vertical layout  
- HTML-only toggle visible & intuitive  

## ⭐ Critical Fixes
- Installer now packages the correct latest EXE  
- Browser detection interpolation fix  
- Cleaned unused variables  
- Improved async usage and file IO safety  
- Wrapped all file writes in reliable error handling  

---

# ⚡ Quick Start

## GUI
1. Install using EXE/MSI  
2. Open **Bookmark Backup Tool**  
3. Select browsers  
4. Click **Export** or **Import**  

## CLI (same for Full & Lite)
```
BookmarkBackupTool.exe --help
```

### Common Commands
```powershell
BookmarkBackupTool.exe --export --all-browsers
BookmarkBackupTool.exe --export --all-browsers --zip
BookmarkBackupTool.exe --export --all-browsers --html
```
---
### Import
```powershell
BookmarkBackupTool.exe --import --path "Bookmarks.json"
BookmarkBackupTool.exe --import --chrome --path "ChromeBackup.json"
BookmarkBackupTool.exe --import --path "Backup.zip"
```

### (Full Edition) Create daily 2AM backup task
```powershell
BookmarkBackupTool.exe --create-task --frequency Daily --time 02:00 --all-browsers
```

# 🌟 Core Features

- Multi-browser backup: Chrome, Edge, Firefox  
- Auto-detect browser from file extension/filename  
- Smart file filtering in dialogs  
- Automatic backups before import  
- HTML, JSON, SQLite, ZIP support  
- Multi-profile support  
- Enterprise logging  
- Smart network path detection  
- Roaming profile support  
- Zero-dependency, self-contained executable  

---

# 📥 Installation

## Option 1 — EXE Installer
Recommended for most users.

## Option 2 — MSI Installer
Recommended for IT departments.

### Silent Install (Enterprise)
```powershell
BookmarkBackupTool-Full-Setup.exe /SILENT
```
or
```powershell
msiexec /i BookmarkBackupTool-Full-v2.3.0.msi /quiet /norestart
```

---

# 💻 Command Line Interface

The CLI is identical between GUI and command-line versions.

### Information Commands
```powershell
BookmarkBackupTool.exe --help
BookmarkBackupTool.exe --version
BookmarkBackupTool.exe --status
BookmarkBackupTool.exe --list-profiles
```

### Export Examples
```powershell
BookmarkBackupTool.exe --export --chrome
BookmarkBackupTool.exe --export --all-browsers --zip
BookmarkBackupTool.exe --export --all-browsers --html
BookmarkBackupTool.exe --export --all-browsers --path "D:\Backups"
```

### Import Examples
```powershell
BookmarkBackupTool.exe --import --path "Bookmarks.html"
BookmarkBackupTool.exe --import --path "BookmarkBackup.zip"
```

### Validation & Repair
```powershell
BookmarkBackupTool.exe --validate "Bookmarks.json"
BookmarkBackupTool.exe --repair "Bookmarks.json"
BookmarkBackupTool.exe --cleanup-logs
```

---

# 📅 Scheduled Tasks (Full Edition Only)

### Create tasks
```powershell
BookmarkBackupTool.exe --create-task --frequency Daily --time 02:00 --all-browsers
BookmarkBackupTool.exe --create-task --frequency Weekly --time 22:00
BookmarkBackupTool.exe --create-task --frequency Monthly --time 01:00
```

### Manage tasks
```powershell
BookmarkBackupTool.exe --view-task
BookmarkBackupTool.exe --modify-task --frequency Daily --time 03:00
BookmarkBackupTool.exe --delete-task
```

---

# 🏢 Enterprise Deployment Examples

### Network backup
```powershell
BookmarkBackupTool.exe --export --all-browsers --zip --path "\\Server\Backups\$env:USERNAME"
```

### Migration
```powershell
BookmarkBackupTool.exe --export --all-browsers --zip --path "\\Share\User"
BookmarkBackupTool.exe --import --path "\\Share\User\Backup.zip"
```

### PowerShell CI scripts
```powershell
BookmarkBackupTool.exe --export --all-browsers
if ($LASTEXITCODE -ne 0) { throw "Backup failed." }
```

---

# 🔧 Configuration File

Stored at:
```
%APPDATA%\BookmarkBackupTool\config.json
```

Example:
```json
{
  "DefaultPath": "C:\\Backups",
  "PreferNetworkPath": true,
  "DefaultBrowsers": ["Chrome", "Edge", "Firefox"],
  "AutoBackupBeforeImport": true,
  "CompressBackups": false,
  "LogRetentionDays": 30
}
```

### MSIX
```powershell
powershell -File scripts\package-msix.ps1 -CertPath ... -CertPassword ...
```

---

# 📈 Exit Codes

| Code | Description |
|------|-------------|
| 0 | Success |
| 1 | Invalid arguments |
| 2 | Import/export failure |
| 3 | Task creation/modification failure |
| 4 | File not found |
| 5 | Permission denied |
| 6 | Configuration error |
| 7 | Browser running (import blocked) |
| 8 | Validation failed |
| 9 | Repair failed |

---

# 🔐 Security
  
- Validates all input files  
- Automatic backups before modifying anything  
- Local-only operations  

Report vulnerabilities:  
*file an issue**

---

---

# 📄 License

MIT License
---

 🎉 Thanks for using Bookmark Backup Tool!
