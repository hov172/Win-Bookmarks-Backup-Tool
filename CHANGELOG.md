# 📝 Changelog - Bookmark Backup Tool

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [2.0.0] - 2025-10-10 🎉 **MAJOR RELEASE**

### 🚀 **Added - Revolutionary Features**

#### **Self-Contained Deployment**
- **Zero-dependency installers** - No .NET Runtime or redistributables required
- **Universal Windows compatibility** - Works on any Windows 10/11 machine
- **Single-file executables** - All dependencies bundled (~101MB each)
- **Offline installation** - No internet connection needed

#### **Professional Installer Suite**
- **EXE Installers (Inno Setup 6)** - Professional user-friendly installers
- **MSI Installers (WiX Toolset)** - Enterprise-ready Windows Installer packages  
- **PATH Environment Integration** - CLI commands work globally after installation
- **Professional Branding** - Custom icons in installer and Windows Control Panel
- **Clean Uninstallation** - Complete removal including environment variables

#### **Dual Edition Strategy**
- **Full Edition** - Complete feature set with automated scheduling
- **Lite Edition** - Core functionality without scheduler (conditional compilation)
- **Identical CLI interfaces** - Both editions support same command structure
- **Size optimization** - Lite edition excludes scheduler code at compile time

#### **Complete CLI Revolution** 
- **100% GUI Parity** - Every GUI feature available via command line
- **Global CLI Access** - Commands work from any directory after installation
- **Enterprise Automation** - Perfect for scripts, GPO, and deployment
- **PowerShell Compatible** - Native Windows PowerShell support

#### **Advanced CLI Commands**
- **Information Commands**: `--help`, `--version`, `--status`, `--list-profiles`
- **Backup Operations**: `--export`, `--import` with full parameter support
- **Task Management**: `--create-task`, `--view-task`, `--modify-task`, `--delete-task` *(Full Edition)*
- **Maintenance**: `--validate`, `--repair`, `--cleanup-logs`
- **Enterprise Features**: Detailed exit codes, error handling, logging

#### **Enhanced User Interface**
- **12-Hour Time Format** - Consistent h:mm:ss tt format across all UI elements
- **Professional Application Icon** - Custom bookmark-themed branding
- **Activity Log Improvements** - Standardized time formatting and better readability
- **Task Management UI** - Complete CRUD interface for scheduled tasks *(Full Edition)*

### 🔧 **Changed - Major Improvements**

#### **Architecture Overhaul**
- **Self-contained publishing** - Moved from framework-dependent to self-contained
- **Conditional compilation** - Lite version built with `LITE_VERSION` preprocessor directive
- **Professional build pipeline** - Automated installer generation for both editions
- **PATH integration** - System environment variable management

#### **Task Scheduling Enhancement**
- **User-level task creation** - No administrator privileges required
- **Reliable task modification** - Improved task recreation approach for schedule changes
- **Enhanced error handling** - Better feedback for task operations
- **Network environment support** - Improved compatibility with domain environments

#### **CLI Command Structure**
- **Standardized parameters** - Consistent naming across all commands
- **Improved help system** - Comprehensive documentation with examples
- **Better error reporting** - Detailed exit codes and error messages
- **Path handling improvements** - Enhanced path validation and fallback logic

#### **Build and Deployment**
- **Professional installer scripts** - Inno Setup and WiX configurations
- **Automated build process** - Single-command build for all installer types
- **Icon integration** - Proper icon handling in installers and applications
- **Environment variable management** - Automatic PATH setup and cleanup

### 🐛 **Fixed - Critical Resolutions**

#### **Task Scheduling Fixes**
- **Network drive compatibility** - Resolved issues with UNC paths and mapped drives
- **Domain environment support** - Fixed task creation in Active Directory environments  
- **PowerShell execution** - Corrected schtasks command syntax issues
- **Task modification reliability** - Implemented stable task recreation approach

#### **Path and Environment Fixes**
- **Roaming profile support** - Enhanced detection of network-redirected profiles
- **Fallback path hierarchy** - Documents → AppData → Temp directory chain
- **UNC path validation** - Improved network path detection and handling
- **Environment variable detection** - Better domain and network environment recognition

#### **UI and Time Format Fixes**
- **TimePicker 12-hour format** - Consistent h:mm:ss tt format implementation
- **Activity log time consistency** - Standardized time display across all log entries
- **Status indicator updates** - Real-time reflection of time format changes
- **Cross-platform time handling** - Improved Windows-specific time formatting

#### **CLI Integration Fixes**
- **PowerShell compatibility** - Resolved command execution issues in PowerShell
- **Parameter parsing** - Enhanced command-line argument handling
- **Exit code standardization** - Proper return codes for automation scenarios
- **Error message clarity** - Improved user-friendly error descriptions

### 🗑️ **Removed - Deprecated Features**
- **Framework-dependent deployment** - Replaced with self-contained approach
- **Manual PATH configuration** - Replaced with automatic installer integration
- **Separate build processes** - Consolidated into unified build pipeline

---

## [1.2.0] - 2025-10-09 **CLI Implementation**

### Added
- Complete CLI interface with 100% GUI parity
- Comprehensive help system with `--help` command
- Information commands: `--version`, `--status`, `--list-profiles`
- Import/export operations: `--import`, `--export` with full parameters
- Task management: `--create-task`, `--view-task`, `--modify-task`, `--delete-task`
- Maintenance commands: `--validate`, `--repair`, `--cleanup-logs`
- Custom professional application icon
- Enhanced network environment detection

### Changed
- Improved task scheduling for non-admin users
- Enhanced network path detection and fallback logic
- Better error handling and user feedback
- Modernized UI with professional icon integration

### Fixed
- Task scheduling issues in domain environments
- Network drive and UNC path compatibility
- Command syntax issues with schtasks
- Profile detection in roaming environments

---

## [1.1.0] - 2025-10-08 **Enhanced Task Management**

### Added
- Complete task management UI with CRUD operations
- Task modification and deletion capabilities
- Enhanced network environment detection
- Improved domain detection (DNS-based, registry-based)
- Better error handling for enterprise environments

### Changed
- Task scheduling approach for better reliability
- Network path detection algorithms
- User interface improvements for task management

### Fixed
- Task creation failures in certain network environments
- Profile path detection issues
- Task modification reliability problems

---

## [1.0.0] - 2025-10-07 **Initial Release**

### Added
- Core bookmark backup and restore functionality
- Support for Chrome, Edge, and Firefox browsers
- Multiple browser profile detection
- Basic scheduled task creation
- ZIP compression for backups
- Avalonia UI for modern Windows interface
- Basic logging and error handling

### Features
- Export bookmarks from multiple browsers
- Import bookmarks to restore functionality
- Simple task scheduling for automated backups
- Clean, modern user interface
- Basic validation and repair capabilities

---

## 📋 **Version Numbering**

This project follows [Semantic Versioning](https://semver.org/):
- **MAJOR** version (X.0.0): Incompatible API changes or major feature overhauls
- **MINOR** version (0.X.0): New functionality added in backwards-compatible manner  
- **PATCH** version (0.0.X): Backwards-compatible bug fixes

## 🎯 **Edition Differences by Version**

| **Feature** | **Full Edition** | **Lite Edition** | **Since Version** |
|-------------|------------------|------------------|-------------------|
| **Bookmark Import/Export** | ✅ | ✅ | 1.0.0 |
| **CLI Interface** | ✅ | ✅ | 1.2.0 |
| **Validation/Repair** | ✅ | ✅ | 1.0.0 |
| **Automated Scheduling** | ✅ | ❌ | 1.0.0 |
| **Task Management CLI** | ✅ | ❌ | 1.2.0 |
| **Self-Contained Deployment** | ✅ | ✅ | 2.0.0 |
| **PATH Integration** | ✅ | ✅ | 2.0.0 |
| **Professional Installers** | ✅ | ✅ | 2.0.0 |

---

**For detailed installation instructions, see [INSTALLATION.md](INSTALLATION.md)**  
**For complete feature documentation, see [README.md](README.md)**