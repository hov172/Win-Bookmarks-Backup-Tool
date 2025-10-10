# 📦 Bookmark Backup Tool - Installation Guide

## 🚀 Professional Installers Available

### Download Options

| **Edition** | **EXE Installer** | **MSI Installer** | **File Size** |
|-------------|-------------------|-------------------|---------------|
| **Full Edition** | `BookmarkBackupTool-Full-Setup.exe` | `BookmarkBackupTool-Full-Setup.msi` | ~32.75-37.17 MB |
| **Lite Edition** | `BookmarkBackupTool-Lite-Setup.exe` | `BookmarkBackupTool-Lite-Setup.msi` | ~32.74-37.16 MB |

## ✨ Installer Features

### ⚡ Self-Contained Deployment
- ✅ **Zero Prerequisites** - No .NET Runtime required
- ✅ **Zero Dependencies** - All libraries included  
- ✅ **Universal Compatibility** - Works on any Windows 10/11 machine
- ✅ **Offline Installation** - No internet connection needed

### 🌍 PATH Environment Integration  
- ✅ **Global CLI Access** - Commands work from any directory
- ✅ **Automatic Registration** - Added to system PATH during installation
- ✅ **Clean Uninstall** - PATH entries removed on uninstall
- ✅ **Admin Installation** - System-wide deployment for all users

### 🎨 Professional Branding
- ✅ **Custom Application Icon** - Professional bookmark-themed branding
- ✅ **Control Panel Integration** - Proper icon in Programs & Features
- ✅ **Start Menu Shortcuts** - Organized under "BookmarkTools" folder
- ✅ **Desktop Shortcut** - Optional during installation

## 📥 Installation Methods

### Method 1: EXE Installer (Recommended for Individual Users)

**Interactive Installation:**
```powershell
# Download and run installer
BookmarkBackupTool-Full-Setup.exe
```

**Silent Installation:**
```powershell
# Silent install for automation
BookmarkBackupTool-Full-Setup.exe /SILENT
BookmarkBackupTool-Full-Setup.exe /VERYSILENT
```

### Method 2: MSI Installer (Enterprise/IT Deployment)

**Interactive Installation:**
```powershell
# Standard MSI installation
msiexec /i BookmarkBackupTool-Full-Setup.msi
```

**Silent Installation:**
```powershell
# Silent install for Group Policy deployment
msiexec /i BookmarkBackupTool-Full-Setup.msi /quiet /norestart

# With logging for troubleshooting
msiexec /i BookmarkBackupTool-Full-Setup.msi /quiet /norestart /l*v install.log
```

**Advanced MSI Parameters:**
```powershell
# Custom installation directory
msiexec /i BookmarkBackupTool-Full-Setup.msi INSTALLFOLDER="C:\CustomPath\BookmarkTool" /quiet

# Install without desktop shortcut
msiexec /i BookmarkBackupTool-Full-Setup.msi DESKTOPSHORTCUT="" /quiet
```

## 🏢 Enterprise Deployment

### Group Policy Deployment (GPO)
1. **Copy MSI files** to a network share accessible by all computers
2. **Open Group Policy Management Console**
3. **Navigate to**: Computer Configuration → Policies → Software Settings → Software Installation
4. **Right-click** and select "New" → "Package"
5. **Browse** to the MSI file on the network share
6. **Select "Advanced"** deployment method for custom options
7. **Apply** and wait for policy refresh

### PowerShell Mass Deployment
```powershell
# Deploy to multiple computers
$computers = @("PC001", "PC002", "PC003")
$msiPath = "\\FileServer\Software\BookmarkBackupTool-Full-Setup.msi"

foreach ($computer in $computers) {
    Write-Host "Installing on $computer..."
    
    Invoke-Command -ComputerName $computer -ScriptBlock {
        param($msi)
        
        # Install silently
        Start-Process -FilePath "msiexec.exe" -ArgumentList "/i `"$msi`" /quiet /norestart" -Wait
        
        # Verify installation
        $installed = Get-WmiObject -Class Win32_Product | Where-Object {$_.Name -like "*Bookmark Backup Tool*"}
        if ($installed) {
            Write-Output "✅ Installation successful on $env:COMPUTERNAME"
            
            # Test CLI access
            & "BookmarkBackupTool-Full" --version
        } else {
            Write-Output "❌ Installation failed on $env:COMPUTERNAME"
        }
    } -ArgumentList $msiPath
}
```

## 🔧 Post-Installation Verification

### Verify Installation Success
```powershell
# Check if application is installed
Get-WmiObject -Class Win32_Product | Where-Object {$_.Name -like "*Bookmark Backup Tool*"}

# Verify CLI access works globally
BookmarkBackupTool-Full --version
BookmarkBackupTool-Full --help

# Check PATH integration
$env:PATH -split ';' | Where-Object {$_ -like "*Bookmark*"}
```

### First Run Configuration
```powershell
# Check system status
BookmarkBackupTool-Full --status

# List available browser profiles  
BookmarkBackupTool-Full --list-profiles

# Test basic export functionality
BookmarkBackupTool-Full --export --chrome --path="C:\temp\test-backup"
```

## 🗑️ Uninstallation

### GUI Uninstall
1. **Open Settings** → Apps → Installed apps (Windows 11)
2. **Or Control Panel** → Programs → Uninstall a program (Windows 10)
3. **Find "Bookmark Backup Tool"** and click Uninstall
4. **Follow prompts** to complete removal

### Command Line Uninstall
```powershell
# Uninstall via MSI product code
$app = Get-WmiObject -Class Win32_Product | Where-Object {$_.Name -like "*Bookmark Backup Tool*"}
$app.Uninstall()

# Or using MSI file directly
msiexec /x BookmarkBackupTool-Full-Setup.msi /quiet
```

## 🔍 Troubleshooting Installation

### Common Issues and Solutions

**❌ "Administrator privileges required"**
```powershell
# Solution: Run installer as Administrator
Start-Process BookmarkBackupTool-Full-Setup.exe -Verb RunAs
```

**❌ "MSI installation failed with error 1603"**
```powershell
# Solution: Enable detailed logging
msiexec /i BookmarkBackupTool-Full-Setup.msi /l*v detailed.log
# Check detailed.log for specific error information
```

**❌ CLI commands not found after installation**
```powershell
# Solution: Restart PowerShell/Command Prompt or refresh environment
$env:PATH = [System.Environment]::GetEnvironmentVariable("PATH", "Machine")
```

**❌ Installation hangs or freezes**
- **Close all browser instances** before installation
- **Temporarily disable antivirus** during installation
- **Run installer from local drive** (not network share)

### Installation Logs
- **EXE Installer logs**: Windows Event Viewer → Applications and Services Logs
- **MSI Installer logs**: Use `/l*v logfile.txt` parameter for detailed logging
- **Application logs**: `%LOCALAPPDATA%\BookmarkTool\logs\BookmarkTool.log`

## 📞 Support Information

### System Information for Support
```powershell
# Gather system info for support requests
Write-Host "OS Version: $((Get-WmiObject Win32_OperatingSystem).Caption)"
Write-Host "Architecture: $env:PROCESSOR_ARCHITECTURE"
Write-Host "PowerShell Version: $($PSVersionTable.PSVersion)"
BookmarkBackupTool-Full --version
BookmarkBackupTool-Full --status
```

---

**Need help?** Check the main [README.md](README.md) for comprehensive documentation and troubleshooting guides.