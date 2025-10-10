# 📖 Windows Bookmark Backup Tool Professional

-**Still beta testing**

[![Platform](https://img.shields.io/badge/Platform-Windows%2010/11-blue.svg)](https://docs.microsoft.com/en-us/windows/)
[![Release](https://img.shields.io/badge/Release-v2.0.0-green.svg)](https://github.com/your-repo/releases)
[![Enterprise Ready](https://img.shields.io/badge/Enterprise-MSI%20%2B%20EXE-red.svg)](#-professional-installers)

**Professional-grade Windows application for comprehensive browser bookmark management, backup, and automation.** Built with Avalonia UI for native Windows 10/11 performance. Features complete CLI support with 100% GUI parity, automated scheduling, and enterprise deployment options.

## 🎯 **Two Editions Available**

✅ **Self-Contain**
- BoomarkBackupTool-Full.exe - Self-contain with Scheduled 
- BackupBoomarkBackupTool-Lite.exe - Self-contain without Scheduled Backup

✅ **MsI Installer**
- oomarkBackupTool-Full-Setup.msi - with Scheduled Backup
- ackupBoomarkBackupTool-Lite-Setup.msi - Without Scheduled Backup 

### 📦 **Full Edition** - Complete Professional Suite
- ✅ **Complete Bookmark Management** - Import, export, validate, and repair
- ✅ **Automated Scheduling** - Daily/Weekly/Monthly backup automation  
- ✅ **Complete CLI Interface** - 100% GUI parity for automation
- ✅ **Enterprise Features** - Task management, logging, validation
- ✅ **PATH Integration** - Global CLI commands from anywhere
- **Size**: ~101MB self-contained (32.75MB installer)

### 📦 **Lite Edition** - Core Backup Features
- ✅ **Essential Bookmark Management** - Import, export, validate, repair
- ✅ **Complete CLI Interface** - Same powerful CLI as Full edition
- ✅ **PATH Integration** - Global CLI commands from anywhere
- ❌ **Automated Scheduling** - Scheduler features excluded
- **Size**: ~101MB self-contained (32.74MB installer)

## 🚀 **Professional Installers**

**Zero-dependency, self-contained installers with PATH integration for seamless CLI access.**

### 📥 **Download Options**

| **Installer Type** | **Full Edition** | **Lite Edition** | **Best For** |
|---------------------|------------------|------------------|--------------|
| **EXE (Inno Setup)** | `BookmarkBackupTool-Full-Setup.exe` | `BookmarkBackupTool-Lite-Setup.exe` | Individual users, direct download |
| **MSI (Windows Installer)** | `BookmarkBackupTool-Full-Setup.msi` | `BookmarkBackupTool-Lite-Setup.msi` | Enterprise deployment, Group Policy |

### ✨ **Installer Features**
- ✅ **Zero Prerequisites** - No .NET Runtime or dependencies needed
- ✅ **PATH Integration** - CLI commands work globally after installation
- ✅ **Professional Icons** - Custom icons in installer and Control Panel
- ✅ **Clean Uninstall** - Complete removal including PATH entries
- ✅ **Start Menu Integration** - Professional shortcuts and organization
- ✅ **Admin Installation** - System-wide deployment for all users

### 🏢 **Enterprise Deployment**
```powershell
# Silent installation (IT deployments)
BookmarkBackupTool-Full-Setup.exe /SILENT
msiexec /i BookmarkBackupTool-Full-Setup.msi /quiet

# Verify CLI access after installation
BookmarkBackupTool-Full --version
BookmarkBackupTool-Full --help
```

## 🆕 **Version 2.0.0 - October 2025** 🎉

### � **Major Features**
- **🎯 Self-Contained Deployment** - Zero .NET Runtime dependency
- **🌍 PATH Environment Integration** - Global CLI access from anywhere  
- **🏢 Professional Installers** - Both EXE and MSI formats
- **✨ Complete CLI Parity** - Every GUI feature available via command line
- **⚡ Lite Edition** - Streamlined version without scheduler
- **🎨 Professional Branding** - Custom icons and Windows integration

### 💻 **CLI Revolution**
- **📋 Information Commands**: `--version`, `--status`, `--list-profiles`, `--help`
- **📥📤 Backup Operations**: `--import`, `--export` with full parameter support
- **⏰ Task Management**: `--create-task`, `--view-task`, `--modify-task`, `--delete-task`
- **�️ Maintenance**: `--validate`, `--repair`, `--cleanup-logs`
- **🔧 Enterprise Ready**: Detailed exit codes, PowerShell compatibility

### 🏗️ **Technical Excellence**
- **🔒 User-Level Scheduling** - No administrator privileges required
- **🌐 Network Environment Support** - Domain detection, roaming profiles
- **📍 Intelligent Path Selection** - Smart fallback hierarchy
- **🎨 12-Hour Time Format** - Consistent time display across UI
- **🔄 Conditional Compilation** - Lite version excludes scheduler at build time

## 📋 Table of Contents

- [Recent Updates & Enhancements](#-recent-updates--enhancements)
- [Quick Start](#-quick-start)  
## 📚 **Table of Contents**

- [🚀 Professional Installers](#-professional-installers)
- [🔧 Installation](#-installation) 
- [💻 Command Line Interface - Complete Feature Parity](#-command-line-interface---complete-feature-parity) ⭐ **FEATURED**
- [🏢 Enterprise Automation Examples](#-enterprise-automation-examples)
- [📋 System Requirements](#-system-requirements)
- [✨ Core Features](#-core-features)
- [🔧 Configuration](#-configuration)
- [🏗️ Development](#️-development)
- [📝 Documentation](#-documentation)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)

## 📝 **Documentation**

- **[📖 Complete README](README.md)** - This comprehensive guide
- **[📥 Installation Guide](INSTALLATION.md)** - Detailed setup instructions
- **[📝 Changelog](CHANGELOG.md)** - Version history and updates
- **[🔧 Build Guide](#️-development)** - Development and compilation instructions

### Reporting Issues
When reporting bugs, please include:
- **OS and Version**: Windows 10/11 (specify build number if known)
- **Architecture**: x64 or ARM64
- **Application Version**: Check About dialog or use `--version` flag
- **Steps to Reproduce**: Detailed steps that reproduce the issue
- **Expected vs Actual Behavior**: What should happen vs what actually happens
- **Log Files**: Include relevant log entries from `BookmarkTool.log`

### Pull Request Process
1. **Update** documentation for any new features
2. **Add tests** that verify your changes work correctly
3. **Ensure** all existing tests pass: `dotnet test`
4. **Update** the CHANGELOG.md with details of your changes
5. **Submit** pull request with clear description of changes

### Development Environment Setup
```powershellequirements](#-system-requirements)  
- [Quick Start](#-quick-start)
- [Installation Options](#-installation-options)
- [Command Line Interface](#-command-line-interface)
- [Configuration](#-configuration-file)
- [Build Information](#-build-information)
- [Development](#️-development)
- [FAQ](#-frequently-asked-questions)
- [Troubleshooting](#-troubleshooting)
- [Contributing](#-contributing)
- [License](#-license)

## ⚡ Quick Start

### For End Users (GUI)
1. Download `AvaloniaBookmarkTool-Setup.exe` from the [Releases](https://github.com/your-repo/releases) page
2. Run the installer as administrator  
3. Launch from Start Menu or Desktop shortcut
4. Select browsers and click **📤 Export Bookmarks** to backup bookmarks

### For Power Users & Automation (CLI) ⭐ NEW!
```cmd
# Quick backup of all browsers with ZIP compression
cmd /c "AvaloniaBookmarkTool.exe --export --all-browsers --zip"

# Restore from backup
cmd /c "AvaloniaBookmarkTool.exe --import --path=backup_folder"

# Create daily automated backup task
cmd /c "AvaloniaBookmarkTool.exe --create-task --schedule=02:00 --frequency=Daily"

# View system status and detected profiles  
cmd /c "AvaloniaBookmarkTool.exe --status"
cmd /c "AvaloniaBookmarkTool.exe --list-profiles"
```

### For Developers
```powershell
git clone https://github.com/your-repo/BookmarkBackupTool.git
cd BookmarkBackupTool
dotnet run
```

## 🌟 Features

### Core Functionality
- **Multi-Browser Support**: Chrome, Edge, and Firefox bookmark management
- **Complete CLI Parity**: 100% of GUI features available via command line ⭐ **NEW!**
- **Safe Import/Export**: Prevents operations while browsers are running
- **Enhanced Network Detection**: Comprehensive detection for domain environments and network paths
- **Smart Path Selection**: Intelligent fallback hierarchy (Documents → AppData → Temp)
- **Profile Management**: Handle multiple browser profiles per user
- **ZIP Archive Support**: Optional compression of exported bookmark files
- **Complete Task Scheduling**: Full CRUD operations for automated backup tasks (GUI & CLI)
- **Non-Admin Compatible**: Works perfectly for regular users without administrator privileges
- **Enterprise Automation**: Perfect for scripts, Group Policy deployment, and automated workflows ⭐ **NEW!**

### User Interface & Experience
- **Professional Branding**: Custom bookmark-themed application icon
- **Modern GUI**: Clean, intuitive Avalonia-based interface with enhanced task management
- **Task Management Panel**: Dedicated buttons for Create/View/Modify/Delete scheduled tasks
- **Real-Time Feedback**: Enhanced status messages and operation progress
- **Network Environment Aware**: Automatic detection and display of network/local context
- **Grouped Sections**: Organized layout with browser checkboxes and advanced controls
- **Keyboard Shortcuts**: Alt+E (Export), Alt+I (Import)

### Advanced Features
- **Complete CLI System** ⭐ **NEW!**:
  - Help system: `--help`, `--version`, `--status`, `--list-profiles`
  - Import/Export: `--import`, `--export` with full browser and path options
  - Task Management: `--create-task`, `--view-task`, `--modify-task`, `--delete-task`
  - Maintenance: `--validate`, `--repair`, `--cleanup-logs`
  - Enterprise automation with detailed exit codes and error handling
- **Enterprise Network Support**: 
  - UNC path detection (`\\server\share` patterns)
  - DNS domain validation (e.g., ADMIN.SLC.EDU)
  - Mapped drive detection and registry-based network identification
  - Profile redirection support for roaming user profiles
- **Robust Task Management**:
  - User-level scheduled tasks (no admin privileges required)
  - Task recreation approach for reliable schedule modifications
  - Real-time task status monitoring and execution history (GUI & CLI)
  - Support for Daily/Weekly/Monthly schedules with custom execution times
- **Configuration & Logging**: Persistent settings, comprehensive operation logging with retention policies
- **Safety Features**: Automatic backups before import operations, smart browser process detection

## � Enhanced Task Scheduling & Network Detection

### Task Scheduling (No Admin Required!)
The application now supports **complete task management** without requiring administrator privileges:

- **Create Tasks**: Schedule daily/weekly/monthly bookmark backups
- **View Tasks**: Check current task status, schedule, and execution history  
- **Modify Tasks**: Update schedule frequency and execution time
- **Delete Tasks**: Remove scheduled tasks when no longer needed

**Technical Implementation:**
- Uses **user-level scheduled tasks** (runs under your account)
- **No `/RU SYSTEM`** or elevation parameters required
- **Task recreation approach** for reliable schedule modifications
- **Atomic operations** ensure tasks are safely updated

### Network Environment Detection
**Enterprise-Ready Network Support:**

🏢 **Domain Environment Detection**
- Automatically detects domain membership (e.g., ADMIN.SLC.EDU)
- Identifies domain logon context and user profile redirection
- Supports both domain-joined and workgroup environments

📁 **Intelligent Path Detection**
- **UNC Paths**: Detects `\\server\share` network locations
- **Mapped Drives**: Identifies network-mapped drive letters
- **DNS Validation**: Verifies network domains and connectivity
- **Registry Detection**: Uses Windows registry for network configuration

🔄 **Smart Fallback Hierarchy**
1. **Documents Folder**: `C:\Users\[user]\Documents\BookmarkBackups` (preferred)
2. **AppData Local**: `C:\Users\[user]\AppData\Local\BookmarkBackups` (fallback)
3. **Temp Directory**: System temp location (final fallback)

### Network vs Local Behavior
- **Network Users**: Automatically detects and uses appropriate network-safe paths
- **Local Users**: Uses standard local profile directories
- **Mixed Environments**: Intelligently adapts based on current login context
- **Profile Redirection**: Supports roaming profiles and folder redirection policies

## �📋 System Requirements

- **Operating System**: Windows 10/11 (x64 or ARM64)
- **Architecture**: x64 or ARM64 processors
- **.NET Runtime**: .NET 8.0 Desktop Runtime (for framework-dependent builds only)
- **Disk Space**: 50MB minimum for installation
- **Memory**: 512MB RAM minimum
- **User Privileges**: Standard user account sufficient for all features
- **Administrator Rights**: Only required for "All Users" backup feature

> **Note**: **Scheduled tasks now work for regular users!** Administrator privileges are no longer required for creating automated bookmark backup tasks. The application uses user-level Windows Task Scheduler integration that runs under your own account permissions.

> **Enterprise Note**: This application is designed for Windows environments and includes comprehensive network detection for domain-joined machines, UNC paths, and enterprise profile configurations.

## 🚀 Installation Options

### Option 1: Inno Setup Installer (Recommended)
**File**: `BookmarkBackupTool-Setup.exe` (32.28 MB)
- Professional Windows installer with modern UI
- Installs to `C:\Program Files\BookmarkBackupTool\`
- Creates Start Menu and Desktop shortcuts
- Windows uninstall support via Settings > Apps
- Requires administrator privileges for installation
- Self-contained executable (no .NET runtime required)

### Option 2: MSI Installer (Enterprise)
**File**: `BookmarkBackupTool-New.msi` (2.96 MB)
- Enterprise-friendly MSI format for corporate deployment
- Group Policy and SCCM deployment support
- Windows Installer database integration
- Professional uninstall capabilities through Windows Settings
- Requires administrator privileges for installation
- Self-contained executable (no .NET runtime required)

### Option 3: Portable Executable (Most Popular)
**File**: `SingleFile-x64\BookmarkBackupTool.exe` (74.92 MB)
- No installation required - run from any location
- Self-contained single file with all dependencies
- No .NET runtime dependencies or additional files
- Perfect for USB drives, network shares, or restricted environments
- Can be run from user directory without admin rights

### Option 4: Framework-Dependent (Smallest)
**File**: `FrameworkDependent\BookmarkBackupTool.exe` (0.15 MB)
- Requires .NET 8.0 Desktop Runtime to be installed
- Smallest download size for environments with .NET 8.0
- Perfect for corporate environments with centralized .NET management

## � **Installation**

### 🚀 **Quick Installation**

**Option 1: EXE Installer (Recommended for Individual Users)**
1. Download `BookmarkBackupTool-Full-Setup.exe` or `BookmarkBackupTool-Lite-Setup.exe`
2. Run installer as Administrator
3. CLI commands available globally: `BookmarkBackupTool-Full --help`

**Option 2: MSI Installer (Enterprise/IT Deployment)**
```powershell
# Interactive installation
msiexec /i BookmarkBackupTool-Full-Setup.msi

# Silent installation for deployment
msiexec /i BookmarkBackupTool-Full-Setup.msi /quiet /norestart
```

### ✨ **Post-Installation Features**
- ✅ **PATH Integration**: CLI commands work from any directory
- ✅ **Start Menu Shortcuts**: Professional integration
- ✅ **Proper Uninstall**: Clean removal via Control Panel
- ✅ **Application Icon**: Professional branding in Control Panel

---

## 💻 **Command Line Interface - Complete Feature Parity**

**100% CLI parity with GUI features!** Every graphical function available via command line for automation, scripting, and enterprise deployment. **Commands work globally after installation thanks to PATH integration.**

### 🎯 **Global CLI Access** 
```powershell
# After installation, commands work from anywhere:
BookmarkBackupTool-Full --help          # Full Edition
BookmarkBackupTool-Lite --version       # Lite Edition

# No need for full paths - PATH integration included!
```

### 🔧 **Edition Differences**
| **Command Category** | **Full Edition** | **Lite Edition** |
|---------------------|------------------|------------------|
| **Information Commands** | ✅ All supported | ✅ All supported |
| **Import/Export** | ✅ All supported | ✅ All supported |
| **Validation/Repair** | ✅ All supported | ✅ All supported |
| **Task Management** | ✅ Full scheduler | ❌ Not available |
| **Task Commands** | ✅ --create-task, --view-task, etc. | ❌ Excluded |

### 📖 **Complete Command Reference**

#### **Information & System Commands**
```powershell
# Comprehensive help with all commands and examples
BookmarkBackupTool-Full --help

# Version information and build details  
BookmarkBackupTool-Full --version

# List all detected browser profiles
BookmarkBackupTool-Full --list-profiles

# System status, tasks, and health check
BookmarkBackupTool-Full --status
```

#### **Backup & Restore Operations**
```powershell
# Export bookmarks from all browsers to default location
BookmarkBackupTool-Full --export --all-browsers

# Export with ZIP compression for easy distribution  
BookmarkBackupTool-Full --export --all-browsers --zip

# Export to specific directory
BookmarkBackupTool-Full --export --all-browsers --path="D:\MyBackups"

# Export specific browsers only
BookmarkBackupTool-Full --export --chrome --edge

# Export all profiles (not just default)
BookmarkBackupTool-Full --export --all-browsers --all-profiles

# Import bookmarks from backup directory
BookmarkBackupTool-Full --import --path="D:\MyBackups"

# Import with validation and repair
BookmarkBackupTool-Full --import --path="D:\MyBackups" --validate

# Import from backup location
cmd /c "AvaloniaBookmarkTool.exe --import --path=D:\MyBackups"

```

#### **📅 Scheduled Task Management** *(Full Edition Only)*
```powershell
# Create daily backup task at 2:00 AM
BookmarkBackupTool-Full --create-task --schedule="02:00" --frequency="Daily"

# Create weekly backup every Sunday at 10:00 PM  
BookmarkBackupTool-Full --create-task --schedule="22:00" --frequency="Weekly"

# Create monthly backup on 1st day at 1:00 AM
BookmarkBackupTool-Full --create-task --schedule="01:00" --frequency="Monthly"

# View current scheduled task details
BookmarkBackupTool-Full --view-task

# Modify existing task to run at 3:00 AM daily
BookmarkBackupTool-Full --modify-task --schedule="03:00" --frequency="Daily"

# Delete the scheduled backup task
BookmarkBackupTool-Full --delete-task
```

#### **🔧 Validation & Maintenance**
```powershell
# Validate bookmark files in directory
BookmarkBackupTool-Full --validate --path="D:\Backups"

# Repair corrupted bookmark files
BookmarkBackupTool-Full --repair --path="D:\Backups"

# Clean up old log files (older than 30 days)  
BookmarkBackupTool-Full --cleanup-logs
```

### 🏢 **Enterprise Automation Examples**

#### **Corporate Backup Scenarios**
```powershell
# Daily automated backup to network share
BookmarkBackupTool-Full --export --all-browsers --all-profiles --zip --path="\\BackupServer\Users\$env:USERNAME"

# Deploy standardized backup schedule company-wide
BookmarkBackupTool-Full --create-task --schedule="02:00" --frequency="Daily"

# IT maintenance: validate and cleanup logs
BookmarkBackupTool-Full --validate --path="\\BackupServer\Users\$env:USERNAME"
BookmarkBackupTool-Full --cleanup-logs
```

#### **Batch Deployment Script**
```powershell
# Enterprise deployment script example
foreach ($computer in $computers) {
    # Silent install
    Invoke-Command -ComputerName $computer -ScriptBlock {
        msiexec /i "BookmarkBackupTool-Full-Setup.msi" /quiet /norestart
        
        # Configure after installation
        BookmarkBackupTool-Full --create-task --schedule="02:00" --frequency="Daily"
        BookmarkBackupTool-Full --status
    }
}
```

---

## � **System Requirements**

### **Minimum Requirements**
- **OS**: Windows 10 version 1809 (build 17763) or Windows 11
- **Architecture**: x64 (Intel/AMD 64-bit)
- **RAM**: 512 MB available memory
- **Storage**: 150 MB free disk space
- **Dependencies**: **NONE** - Self-contained deployment

### **Supported Browsers**
- ✅ **Google Chrome** (all versions, multiple profiles)
- ✅ **Microsoft Edge** (Chromium-based, all versions)  
- ✅ **Mozilla Firefox** (all versions, multiple profiles)
- ✅ **Automatic Detection** - Profiles found automatically

### **Enterprise Features**
- ✅ **Domain Environments** - Full support for AD domains
- ✅ **Roaming Profiles** - Network profile compatibility
- ✅ **Group Policy** - MSI deployment via GPO
- ✅ **Network Shares** - UNC path backup destinations
- ✅ **User-Level Tasks** - No admin rights required for scheduling

#### Enterprise Automation Scenarios
```cmd
# Daily automated backup for corporate environment
cmd /c "AvaloniaBookmarkTool.exe --export --all-browsers --all-profiles --zip --path=\\BackupServer\Users\%USERNAME%"

# Create standardized backup task for all users
cmd /c "AvaloniaBookmarkTool.exe --create-task --schedule=02:00 --frequency=Daily"

# System maintenance: validate and cleanup
cmd /c "AvaloniaBookmarkTool.exe --validate --path=\\BackupServer\Users\%USERNAME%" && cmd /c "AvaloniaBookmarkTool.exe --cleanup-logs"
```

#### Development & Testing Workflows
```cmd
# Check what would be exported (dry run equivalent)
cmd /c "AvaloniaBookmarkTool.exe --list-profiles"
cmd /c "AvaloniaBookmarkTool.exe --status"

# Export for testing with specific browsers
cmd /c "AvaloniaBookmarkTool.exe --export --chrome --path=D:\TestBackups"

# Validate test backup files
cmd /c "AvaloniaBookmarkTool.exe --validate --path=D:\TestBackups"
```

#### Recovery & Migration Scenarios
```cmd
# Full system backup before migration
cmd /c "AvaloniaBookmarkTool.exe --export --all-browsers --all-profiles --zip --path=D:\Migration\Bookmarks"

# Restore bookmarks on new system
cmd /c "AvaloniaBookmarkTool.exe --import --path=D:\Migration\Bookmarks\backup.zip"

# Verify successful migration
cmd /c "AvaloniaBookmarkTool.exe --list-profiles"
cmd /c "AvaloniaBookmarkTool.exe --validate --path=%USERPROFILE%\Desktop"
```

#### Network & Remote Operations
```cmd
# Backup to network share
cmd /c "AvaloniaBookmarkTool.exe --export --all-browsers --zip --path=\\FileServer\Backups\%COMPUTERNAME%"

# Import from cloud storage
cmd /c "AvaloniaBookmarkTool.exe --import --path=C:\OneDrive\BookmarkBackups"

# Corporate scheduled backup to UNC path
cmd /c "AvaloniaBookmarkTool.exe --create-task --schedule=01:30 --frequency=Daily"
```

### 📊 Exit Codes & Error Handling

The CLI returns specific exit codes for precise automation control:

| Exit Code | Meaning | Description |
|-----------|---------|-------------|
| **0** | Success | Operation completed successfully |
| **1** | Invalid Arguments | Command syntax error or invalid parameters |
| **2** | Operation Failed | Export/import operation failed |
| **3** | Task Operation Failed | Scheduled task creation/modification failed |
| **4** | File Not Found | Specified files or paths don't exist |
| **5** | Permission Denied | Insufficient permissions for operation |
| **6** | Configuration Error | Invalid configuration or settings |
| **7** | Browser Running | Import blocked (browsers must be closed) |
| **8** | Validation Failed | Bookmark file validation failed |
| **9** | Repair Failed | Bookmark file repair operation failed |

#### PowerShell Error Handling Example
```powershell
# PowerShell script with error handling
$result = cmd /c "AvaloniaBookmarkTool.exe --export --all-browsers --zip"
if ($LASTEXITCODE -eq 0) {
    Write-Host "✅ Backup completed successfully" -ForegroundColor Green
} elseif ($LASTEXITCODE -eq 7) {
    Write-Host "⚠️ Please close all browsers and try again" -ForegroundColor Yellow
} else {
    Write-Host "❌ Backup failed with exit code: $LASTEXITCODE" -ForegroundColor Red
    exit $LASTEXITCODE
}
```

#### Batch Script Error Handling Example
```batch
@echo off
cmd /c "AvaloniaBookmarkTool.exe --export --all-browsers --zip"
if %ERRORLEVEL% equ 0 (
    echo ✅ Backup successful
) else if %ERRORLEVEL% equ 7 (
    echo ⚠️ Close browsers and retry
) else (
    echo ❌ Backup failed with code %ERRORLEVEL%
    exit /b %ERRORLEVEL%
)
```

### 🚀 CLI Best Practices

#### For System Administrators
```cmd
# Create standardized backup script for deployment
@echo off
echo Creating daily backup task...
cmd /c "AvaloniaBookmarkTool.exe --create-task --schedule=02:00 --frequency=Daily"
if %ERRORLEVEL% equ 0 (
    echo ✅ Backup task created successfully
    cmd /c "AvaloniaBookmarkTool.exe --view-task"
) else (
    echo ❌ Failed to create backup task
)
```

#### For Automated Workflows
```cmd
# Complete backup and validation workflow
cmd /c "AvaloniaBookmarkTool.exe --export --all-browsers --zip --path=\\BackupServer\Users\%USERNAME%"
if %ERRORLEVEL% equ 0 (
    cmd /c "AvaloniaBookmarkTool.exe --validate --path=\\BackupServer\Users\%USERNAME%"
    if %ERRORLEVEL% equ 0 (
        cmd /c "AvaloniaBookmarkTool.exe --cleanup-logs"
        echo ✅ Complete backup workflow successful
    )
)
```

#### For Personal Use
```cmd
# Simple weekly backup routine
cmd /c "AvaloniaBookmarkTool.exe --export --all-browsers --zip --path=%USERPROFILE%\Desktop\BookmarkBackups"
echo Backup completed. Files saved to Desktop\BookmarkBackups
```

### 💡 CLI Tips & Tricks

1. **PowerShell Compatibility**: Always use `cmd /c` wrapper for reliable output
2. **Path Handling**: Use quotes around paths with spaces: `--path="C:\My Folder\Backups"`
3. **Network Paths**: UNC paths work directly: `--path=\\server\share\backups`
4. **Batch Operations**: Combine multiple commands for complete workflows
5. **Error Checking**: Always check exit codes for reliable automation
6. **Task Management**: Use `--view-task` to verify task creation before relying on automation
7. **Testing**: Use `--list-profiles` and `--status` to verify system state before operations
```

#### Backup and Recovery Examples
```powershell
# Create backup without importing
BookmarkBackupTool.exe --backup-only --chrome --path "D:\SafeBackups"

# Import without creating backup (risky)
BookmarkBackupTool.exe --import --no-backup --path "bookmarks.html"

# Validate bookmark file before importing
BookmarkBackupTool.exe --validate --path "suspicious_bookmarks.html"

# Attempt to repair corrupted bookmark file
BookmarkBackupTool.exe --repair --path "corrupted_bookmarks.html"
```

#### Scheduled Task Examples (Windows)
```powershell
# Create daily backup at 2 AM
BookmarkBackupTool.exe --create-task --schedule "02:00" --frequency Daily --task-name "DailyBookmarkBackup"

# Create weekly backup every Sunday at 10 PM
BookmarkBackupTool.exe --create-task --schedule "22:00" --frequency Weekly --task-name "WeeklyBackup"

# Remove existing scheduled task
BookmarkBackupTool.exe --remove-task --task-name "DailyBookmarkBackup"

# Create task with specific browsers and ZIP compression
BookmarkBackupTool.exe --create-task --chrome --edge --zip --schedule "01:00" --frequency Daily
```

#### Automation and Scripting Examples
```powershell
# Complete automated backup workflow
BookmarkBackupTool.exe --silent --export --all-browsers --all-profiles --zip --path "\\NetworkShare\Backups" --log-level Info

# Corporate environment: Export all users (requires admin)
BookmarkBackupTool.exe --export --all-users --all-browsers --path "\\Server\UserBackups" --zip --log-file "\\Server\Logs\bookmark_backup.log"

# Development testing: Dry run with maximum verbosity
BookmarkBackupTool.exe --dry-run --verbose --export --all-browsers --all-profiles --zip

# Emergency recovery: Force import even if browsers running
BookmarkBackupTool.exe --import --force --path "emergency_backup.zip" --verbose
```

#### Cross-Browser Operations
```powershell
# Export each browser to separate files
BookmarkBackupTool.exe --export --chrome --path "D:\Backups\chrome_bookmarks.html"
BookmarkBackupTool.exe --export --edge --path "D:\Backups\edge_bookmarks.html"  
BookmarkBackupTool.exe --export --firefox --path "D:\Backups\firefox_bookmarks.html"

# Import different formats
BookmarkBackupTool.exe --import --chrome --path "chrome_bookmarks.html"
BookmarkBackupTool.exe --import --firefox --path "firefox_bookmarks.json"
BookmarkBackupTool.exe --import --edge --path "edge_bookmarks.zip"
```

#### Network and Remote Operations
```powershell
# Backup to network share
BookmarkBackupTool.exe --export --all-browsers --zip --path "\\FileServer\Backups\%USERNAME%"

# Import from cloud storage location
BookmarkBackupTool.exe --import --all-browsers --path "C:\OneDrive\BookmarkBackups\latest.zip"

# Corporate backup with UNC paths
BookmarkBackupTool.exe --export --all-users --all-browsers --path "\\CorporateNAS\UserData\BookmarkBackups"
```

#### Maintenance and Cleanup Examples
```powershell
# Check application status and configuration
BookmarkBackupTool.exe --status --config "custom_config.json"

# Clean up old log files (if supported)
BookmarkBackupTool.exe --cleanup-logs --log-retention-days 7

# Reset configuration to defaults
BookmarkBackupTool.exe --reset-config --config "config.json"

# Generate configuration template
BookmarkBackupTool.exe --generate-config --path "template_config.json"
```

#### Batch Operations for Multiple Scenarios
```powershell
# Home user: Daily personal backup
BookmarkBackupTool.exe --export --all-browsers --zip --path "%USERPROFILE%\Desktop\BookmarkBackups"

# Power user: Multiple profiles with custom naming
BookmarkBackupTool.exe --export --chrome --profile "Work" --path "D:\Backups\Work_Chrome_%DATE%.html"
BookmarkBackupTool.exe --export --chrome --profile "Personal" --path "D:\Backups\Personal_Chrome_%DATE%.html"

# System administrator: Enterprise deployment
BookmarkBackupTool.exe --silent --export --all-users --all-browsers --zip --path "\\BackupServer\Users\BookmarkBackups\%COMPUTERNAME%" --log-file "\\LogServer\BookmarkTool\%COMPUTERNAME%.log"

# Developer: Testing and validation
BookmarkBackupTool.exe --dry-run --export --all-browsers --all-profiles --verbose --log-level Debug
```

### Return Codes and Error Handling
```powershell
# Check operation success in PowerShell scripts
BookmarkBackupTool.exe --export --all-browsers --zip --silent
if ($LASTEXITCODE -eq 0) {
    Write-Host "Backup completed successfully"
} else {
    echo Backup failed with error code %ERRORLEVEL%
)

# PowerShell error handling
$result = & BookmarkBackupTool.exe --export --all-browsers --zip --silent
if ($LASTEXITCODE -eq 0) {
    Write-Host "Backup successful"
} else {
    Write-Error "Backup failed with code $LASTEXITCODE"
}
```

### Exit Codes
- `0`: Success
- `1`: Invalid arguments or missing action
- `2`: Silent operation failed
- `3`: Scheduled task creation failed

## 🔧 Configuration File

The application uses a JSON configuration file for persistent settings:

**Location**: `%APPDATA%\BookmarkBackupTool\config.json`

### Configuration Options
```json
{
  "DefaultPath": "C:\\Users\\Username\\Desktop",
  "PreferNetworkPath": true,
  "DefaultBrowsers": ["Chrome", "Edge", "Firefox"],
  "AutoBackupBeforeImport": true,
  "VerifyFileIntegrity": true,
  "CreateBackupOnExport": false,
  "CompressBackups": false,
  "LogRetentionDays": 30,
  "ChromeBadgeColor": "#2563EB",
  "EdgeBadgeColor": "#059669",
  "FirefoxBadgeColor": "#D97706",
  "EncryptBackups": false,
  "EncryptionScope": "User"
}
```

### Configuration Properties
- **DefaultPath**: Default export/import directory
- **PreferNetworkPath**: Prefer network paths for shared storage
- **DefaultBrowsers**: Browsers to include when none specified in CLI
- **AutoBackupBeforeImport**: Create backup before importing (default: true)
- **VerifyFileIntegrity**: Validate files before operations (default: true)
- **CompressBackups**: Automatically create ZIP after export
- **LogRetentionDays**: Days to keep log files (default: 30)
- **ChromeBadgeColor/EdgeBadgeColor/FirefoxBadgeColor**: UI badge colors
- **EncryptBackups**: Use Windows DPAPI encryption for ZIP files
- **EncryptionScope**: Encryption scope: "User" or "Machine"

## 📁 Build Information

### Development Builds

#### Framework-Dependent Build
**Location**: `bin\Release\framework-dependent-clean\`
**Size**: ~0.15 MB
**Requirements**: .NET 8.0 Desktop Runtime
**Use Case**: 
- Development and testing
- Systems with .NET runtime already installed
- Minimal disk footprint

#### Self-Contained Build  
**Location**: `bin\Release\self-contained-clean\`
**Size**: ~50 MB (with dependencies)
**Requirements**: None
**Use Case**:
- Deployment without runtime dependencies
- Offline environments
- Custom deployment scenarios

#### Single-File Build (Recommended)
**Location**: `bin\Release\single-file-clean\`
**Size**: 74.9 MB
**Requirements**: None
**Use Case**:
- Portable deployment
- USB/network distribution
- Simplified distribution
- No installation required

### Production Installers

#### Inno Setup Installer (.exe)
**Location**: `bin\Output\BookmarkBackupTool-Setup.exe`
**Size**: 30.46 MB
**Features**:
- Professional Windows installer
- Start Menu and Desktop shortcuts
- Uninstall support
- Registry integration
- Custom installation paths
**Use Case**: Standard Windows software distribution

#### WiX MSI Installer (.msi)
**Location**: `bin\Output\BookmarkBackupTool-Clean.msi`  
**Size**: 108.91 MB
**Features**:
- Enterprise deployment
- Group Policy support
- Windows Installer database
- Silent installation support
- Corporate environment integration
**Use Case**: Enterprise and corporate deployments

### Build Scripts

#### Warning-Free Build Script
**Location**: `BuildAll-Clean.ps1`
**Purpose**: Generate all build variants without warnings
**Usage**: 
```powershell
.\BuildAll-Clean.ps1
```

#### Legacy Build Script
**Location**: `BuildInstallers.ps1`
**Purpose**: Build specific installer types
**Usage**:
```powershell
# Build all installers
.\BuildInstallers.ps1 -All

# Build specific installer
.\BuildInstallers.ps1 -InnoSetup
.\BuildInstallers.ps1 -WiX
.\BuildInstallers.ps1 -NSIS
```

### Development Environment

#### Project Structure
```
AvaloniaBookmarkTool/
├── Assets/
│   └── AppIcon.ico                 # Application icon (766 bytes)
├── Services/                       # Core business logic
│   ├── BookmarkService.cs         # Bookmark operations
│   ├── BrowserPaths.cs           # Browser path detection
│   ├── ConfigService.cs          # Configuration management
│   ├── Logger.cs                 # Logging system
│   ├── ProfilesService.cs        # Profile management
│   ├── SchedulerService.cs       # Task scheduling
│   └── ZipService.cs             # Archive operations
├── Views/                         # UI components
│   ├── MainWindow.axaml          # Main interface
│   └── MainWindow.axaml.cs       # UI logic
├── Installer/                     # Installer configurations
│   ├── InnoSetup/                # Inno Setup scripts
│   ├── WiX/                      # WiX definitions
│   └── NSIS/                     # NSIS scripts
└── bin/                          # Build outputs
    ├── Release/                  # Executable builds
    └── Output/                   # Installer files
```

#### Build Requirements
- .NET 8.0 SDK
- Windows 10/11 SDK
- Inno Setup 6 (for .exe installers)
- WiX Toolset v4/v6 (for .msi installers)
- NSIS (optional, for .exe installers)

## 🛠️ Development

### Building from Source
```powershell
# Clone repository
git clone <repository-url>
cd AvaloniaBookmarkTool

# Restore dependencies
dotnet restore

# Build and run
dotnet run

# Build specific target
dotnet publish AvaloniaBookmarkTool.csproj -c Release -o bin\Release\custom-build
```

### Testing
```powershell
# Run unit tests
dotnet test

# Run with specific configuration
dotnet run --configuration Debug
```

## 🔄 Changelog

### Version 1.2.0 - October 2025 (Current) 🎉
- **✨ MAJOR**: Complete CLI implementation with 100% GUI parity
- **📋 NEW**: Comprehensive help system (`--help`, `--version`)
- **📊 NEW**: System information commands (`--status`, `--list-profiles`)
- **⏰ NEW**: Full task management CLI (`--create-task`, `--view-task`, `--modify-task`, `--delete-task`)
- **🛠️ NEW**: Maintenance utilities (`--validate`, `--repair`, `--cleanup-logs`)
- **🚀 ENHANCED**: Enterprise automation support with detailed exit codes
- **💻 ENHANCED**: PowerShell compatibility with `cmd /c` wrapper approach
- **🔧 ENHANCED**: Professional bookmark-themed application icon
- **🌐 ENHANCED**: Universal network detection for any Windows domain
- **📍 ENHANCED**: Smart path selection with intelligent fallbacks

### Version 1.0.0 (September 2025)
- Initial release with full multi-browser support for Windows
- Avalonia UI implementation with modern Windows design
- Basic command-line interface for export operations
- Scheduled backup functionality using Windows Task Scheduler
- ZIP archive support with compression
- Professional installer packages (.exe and .msi)
- Comprehensive logging system

### Planned Future Versions
- **Version 1.3**: Enhanced PowerShell integration and native cmdlets
- **Version 1.4**: Cloud storage integration (OneDrive, Google Drive, Dropbox)
- **Version 2.0**: Browser extension for one-click backups
- **Version 2.1**: Advanced profile management and enterprise Group Policy support

## ❓ Frequently Asked Questions

### General Usage

**Q: Which browsers are supported?**
A: Google Chrome, Microsoft Edge, and Mozilla Firefox on Windows 10/11.

**Q: Can I backup bookmarks from multiple browser profiles?**
A: Yes, use the `--all-profiles` flag or select specific profiles in the GUI.

**Q: Does the application work while browsers are running?**
A: Export works while browsers are running, but import is blocked for safety. Use `--force` to override (not recommended).

**Q: Where are my backups stored by default?**
A: Desktop folder, or `HOMESHARE` environment variable if available. Customize with `--path` option.

### Installation and Setup

**Q: Do I need administrator rights to install?**
A: Yes, for system-wide installation to `C:\Program Files\`. Use portable version if admin rights unavailable.

**Q: What's the difference between .exe and .msi installers?**
A: .exe (Inno Setup) is for individual users, .msi is for enterprise deployment and Group Policy.

**Q: Can I run without installing?**
A: Yes, use the single-file portable version (`BookmarkBackupTool.exe`) - no installation required.

### Technical Questions

**Q: Do I need .NET installed?**
A: Only for framework-dependent builds. Self-contained and single-file builds include all dependencies.

**Q: How much disk space does it use?**
A: 50-100MB depending on build type. Portable version is ~75MB single file.

**Q: Can I automate backups?**
A: Yes, using command-line interface or Windows scheduled tasks feature.

**Q: What file formats are supported?**
A: HTML, JSON, and ZIP archives. Format depends on browser and export options.

### Troubleshooting

**Q: Application won't start - what should I check?**
A: 1) Check Event Viewer for errors, 2) Verify .NET 8.0 installation, 3) Run as administrator, 4) Check antivirus exclusions.

**Q: Bookmarks not detected - why?**
A: 1) Close all browsers completely, 2) Check browser profile locations, 3) Run as administrator for cross-user access.

**Q: Scheduled tasks not working?**
A: 1) Verify Task Scheduler service running, 2) Check user account permissions, 3) Ensure correct password set.

**Q: Import failed - what went wrong?**
A: 1) Ensure browser is closed, 2) Check file format compatibility, 3) Verify file isn't corrupted, 4) Check disk space.

### Security and Privacy

**Q: Is my data safe?**
A: All operations are local - no data sent to external servers. Backups stored on your system only.

**Q: What permissions does the app need?**
A: File system access for browser profiles, Task Scheduler access for automation (Windows only).

**Q: Can I backup other users' bookmarks?**
A: Yes, with `--all-users` flag, but requires administrator privileges.

## 🎯 Best Practices

### For Home Users
- **Regular Backups**: Set up daily scheduled backups to protect against data loss
- **Multiple Locations**: Store backups on external drives or cloud storage
- **Test Restores**: Periodically test import functionality with backup files
- **ZIP Compression**: Enable ZIP creation to save space and organize backups

### For IT Administrators  
- **Deployment**: Use MSI installer for enterprise-wide deployment via Group Policy
- **Centralized Storage**: Configure network share paths for centralized backup storage
- **Logging**: Enable comprehensive logging for audit trails and troubleshooting
- **Automation**: Implement PowerShell scripts for bulk operations across user accounts

### For Developers
- **Source Builds**: Use framework-dependent builds during development for faster iteration
- **Testing**: Use `--dry-run` and `--validate` flags for safe testing
- **Configuration**: Maintain separate config files for development and production
- **Debugging**: Enable verbose logging and debug log levels for troubleshooting

## 🔐 Security Considerations

- **Administrator Privileges**: Required only for system-wide installation and all-users operations
- **Browser Process Detection**: Prevents data corruption by blocking unsafe operations
- **Backup Creation**: Automatic backups created before import operations to prevent data loss
- **Local Operations**: No network communication - all operations performed locally
- **File Validation**: Input validation prevents malformed bookmark files from causing issues

## 🌍 Internationalization

Currently supports:
- **English** (en-US) - Full support
- **Planned**: Spanish, French, German, Japanese, Chinese (Simplified)

Configuration for additional languages:
```json
{
  "Language": "en-US",
  "DateFormat": "MM/dd/yyyy",
  "TimeFormat": "HH:mm"
}
```

## 🐛 Troubleshooting

### Common Issues & Recent Fixes

#### ✅ **FIXED: "Access is denied" when creating scheduled tasks**
**Previous Issue**: Task creation failed with "ERROR: Access is denied"
**Solution Applied**: 
- Removed `/RU SYSTEM` and `/RL HIGHEST` parameters that required admin privileges
- Tasks now use current user context automatically (no `/RU` parameter needed)
- **Result**: Scheduled tasks work perfectly for regular users without admin rights

#### ✅ **FIXED: "Invalid argument/option - 'FilePath'" error**
**Previous Issue**: Task creation failed with schtasks syntax error
**Solution Applied**:
- Removed complex PowerShell `Start-Process -FilePath` wrapper
- Switched to direct executable path approach: `"app.exe" arguments`
- **Result**: Clean schtasks command syntax that Windows accepts

#### ✅ **FIXED: "Invalid argument/option - '/SC'" when modifying tasks**
**Previous Issue**: Task modification failed because schtasks /Change doesn't support schedule parameters
**Solution Applied**:
- Implemented task recreation approach (delete + create with new parameters)
- Preserves all existing task settings during schedule updates
- **Result**: Reliable task modification that always works

#### ✅ **ENHANCED: Network path detection for enterprise environments**
**Previous Issue**: App couldn't detect network/domain environments properly
**Solution Applied**:
- Added comprehensive network detection (UNC paths, DNS domains, mapped drives)
- Smart path fallback hierarchy for network users
- **Result**: Works seamlessly in domain environments

#### "Application won't start"
- Ensure .NET 8.0 Desktop Runtime is installed (framework-dependent builds)
- Check Windows Event Viewer for detailed error information
- Verify file permissions and antivirus exclusions

#### "Browser bookmarks not detected"
- Run application as administrator for cross-user access
- Check browser profile locations manually
- Ensure browsers are fully closed before import operations

#### **NEW: Task Scheduling Best Practices**
- **No Admin Required**: Standard users can create scheduled tasks for themselves
- **Network Users**: App automatically detects and uses appropriate paths
- **Task Management**: Use View/Modify/Delete buttons for complete task control
- **Troubleshooting Tasks**: Check Windows Task Scheduler (`taskschd.msc`) for detailed task information

### Logging
Application logs are stored at:
- **Windows**: `%APPDATA%\BookmarkBackupTool\BookmarkTool.log`
- **Alternative Windows location**: `C:\Users\[Username]\AppData\Roaming\BookmarkBackupTool\BookmarkTool.log`

## 📝 License

This project is licensed under the MIT License - see the LICENSE.txt file for details.

## 📊 Performance Information

### Benchmark Results
- **Startup Time**: <2 seconds (single-file build)
- **Memory Usage**: 50-100MB RAM during operation
- **Export Speed**: ~1000 bookmarks/second
- **File Size**: Typical backup 1-10MB (varies by bookmark count)

### Scalability
- **Maximum Bookmarks**: No practical limit (tested with 50,000+ bookmarks)
- **Multiple Profiles**: Supports unlimited browser profiles
- **Concurrent Operations**: Single-threaded for safety, but fast enough for all practical uses
- **Large Files**: ZIP compression reduces backup size by 60-80%

### Reporting Issues
When reporting bugs, please include:
- **OS and Version**: Windows 10/11 (specify build number if known)
- **Architecture**: x64 or ARM64
- **Application Version**: Check About dialog or use `--version` flag
- **Steps to Reproduce**: Detailed steps that reproduce the issue
- **Expected vs Actual Behavior**: What should happen vs what actually happens
- **Log Files**: Include relevant log entries from `BookmarkTool.log`

### Pull Request Process
1. **Update** documentation for any new features
2. **Add tests** that verify your changes work correctly
3. **Ensure** all existing tests pass: `dotnet test`
4. **Update** the CHANGELOG.md with details of your changes
5. **Submit** pull request with clear description of changes

### Reporting Security Issues
If you discover a security vulnerability, please:
1. **DO NOT** open a public GitHub issue
2. **Email** security concerns to: [security@your-domain.com]
3. **Include** detailed information about the vulnerability
4. **Wait** for acknowledgment before public disclosure

### Security Features
- **Local Operations Only**: No network communication or data transmission
- **Input Validation**: All file inputs validated to prevent malicious code execution
- **Safe Defaults**: Conservative settings that prioritize data safety
- **Process Isolation**: Browser process detection prevents data corruption

## 📈 Roadmap

### Version 1.1 (Q4 2025)
- **Enhanced Windows Integration**: Better Windows 11 integration and Start Menu experience
- **PowerShell Module**: Native PowerShell cmdlets for enterprise automation
- **Cloud Integration**: OneDrive, Google Drive, Dropbox backup destinations
- **Advanced Scheduling**: More flexible backup scheduling with Windows Task Scheduler

### Version 1.2 (Q1 2026)
- **Browser Extensions**: One-click backup from browser toolbar
- **Real-time Sync**: Automatic backup on bookmark changes detection
- **Advanced Profiles**: Profile-specific settings and configurations
- **Restore Points**: Multiple restore points with timeline view

### Version 2.0 (Q2 2026)
- **Enterprise Features**: Group Policy support and centralized management
- **Windows Store**: Microsoft Store distribution for easier installation
- **API Integration**: REST API for third-party Windows applications
- **Advanced Analytics**: Bookmark usage analytics and insights
- **Plugin System**: Extensible architecture for custom functionality

## 📧 Support and Contact

### Getting Help
- **📧 Email**: [ayala.solutions@gmail.com] for direct support

### Commercial Support
For enterprise support, custom development, or consulting services:
- **Business Email**: [ayala.solutions@gmail.com]


## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE.txt](LICENSE.txt) file for full details.

### Summary
- ✅ **Commercial Use**: You can use this software commercially
- ✅ **Modification**: You can modify and adapt the code
- ✅ **Distribution**: You can distribute original or modified versions
- ✅ **Private Use**: You can use this software privately
- ❗ **Limitation**: Software is provided "as is" without warranty
- ❗ **Attribution**: Original license and copyright notice must be included

---

<div align="center">

**📖 Bookmark Backup Tool v1.2.0**

*Made with ❤️ for the browser user community*

**🚀 Now with Complete CLI Support - 100% GUI Parity!**

**💻 Perfect for GUI Users • 🤖 Perfect for Automation • 🏢 Perfect for Enterprise**

### 🎯 What's New in v1.2.0?

✅ **Complete CLI Implementation** - Every GUI feature now has a CLI equivalent  
✅ **Help & Information** - `--help`, `--version`, `--status`, `--list-profiles`  
✅ **Import/Export Operations** - Full backup and restore via command line  
✅ **Task Management** - Complete CRUD operations for scheduled tasks  
✅ **Maintenance Utilities** - Validation, repair, and cleanup commands  
✅ **Enterprise Ready** - Automation, scripting, and deployment support  

### 🚀 Quick CLI Examples

```cmd
# Get comprehensive help
cmd /c "BookmarkBackupTool.exe --help"

# Export all browsers with ZIP compression
cmd /c "BookmarkBackupTool.exe --export --all-browsers --zip"

# Create daily backup task at 2 AM
cmd /c "BookmarkBackupTool.exe --create-task --schedule=02:00 --frequency=Daily"

# View system status and profiles
cmd /c "BookmarkBackupTool.exe --status"
cmd /c "BookmarkBackupTool.exe --list-profiles"
```

Scheduler via CLI:

    --create-task --frequency=Daily|Weekly|Monthly --schedule=18:00 \
      [--chrome] [--edge] [--firefox] [--all-profiles] [--path=PATH] [--highest] \
      [--run-as-user=DOMAIN\\User] [--run-as-password=Secret]

Notes
-----

- Export creates: `Chrome-Bookmarks.json`, `Edge-Bookmarks.json`, `Firefox-places.sqlite`
- Import validates files and creates backups in `BookmarkTool_Backups` under each profile
- Logs go to `BookmarkTool.log` (target path in silent mode, user profile in GUI)
 - Scheduled tasks use `schtasks` and may require admin rights depending on policy. The task runs with the current GUI selections (browsers, All Profiles, and path). If no browsers are selected, it defaults to all three.
  - Run-as user: if you specify a different user, you likely need to provide the password. The password is only passed to `schtasks` and not stored.
  - Preview Command shows the exact `schtasks` command composed; you can copy/paste it into an elevated Command Prompt for diagnostics.
  - Time can be 24-hour `HH:mm` (e.g., `06:30`, `18:00`) or 12-hour `h:mm tt` (e.g., `6:30 PM`). It is normalized to 24-hour for scheduling.
  - Daily schedules must use a time later than the current time today.
  - GUI Settings: toggle "Create ZIP after export" and set "Log retention (days)", then click "Save Settings". Values persist to `%USERPROFILE%/BookmarkTool.config.json`.
  - Import safety: in GUI you can enable "Force import" to ignore the running-browser check. A confirmation dialog will appear before proceeding.
  - All Windows users export requires running as Administrator and is export-only.
  - Scheduled tasks: GUI also provides a SYSTEM all-users task button (Daily/Weekly/Monthly) using the current browser selections, path, and all-profiles option, running as `SYSTEM`. Optionally randomize minutes to stagger across machines.
  - The Open button opens the most recent `BookmarkBackup_*.zip` in the selected folder when available; otherwise it opens the folder.
  - Badge colors can be set in config, for example: `"ChromeBadgeColor": "#2563EB"`.
  - Config file (optional): `%USERPROFILE%/BookmarkTool.config.json` or pass `--config`. Example:

        {
          "DefaultPath": "D:\\Backups",
          "PreferNetworkPath": true,
          "DefaultBrowsers": ["Chrome", "Edge", "Firefox"],
          "CompressBackups": true,
          "LogRetentionDays": 30
        }
