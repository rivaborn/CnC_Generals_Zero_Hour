# Generals/Code/Tools/Autorun/WinFix.H

## Purpose
Provides OS version detection utilities for Windows systems.

## Responsibilities
- Detects Windows version (9x, NT, 2000, XP)
- Exposes version numbers (major, minor, build)
- Provides system info string
- Checks OS-specific release details

## Key Types
- **WindowsVersionInfo (Class)**: OS version detection and querying
- **WinVersion (Global)**: Singleton instance of WindowsVersionInfo

## Key Functions
### WindowsVersionInfo::Version_String
- Purpose: Returns formatted version string
- Calls: Not inferable

### WindowsVersionInfo::Version_Name
- Purpose: Returns human-readable version name
- Calls: Not inferable

### WindowsVersionInfo::Meets_Minimum_Version_Requirements
- Purpose: Checks if system meets minimum requirements
- Calls: Not inferable

## Globals
- **WinVersion (WindowsVersionInfo)**: Global OS version info instance

## Dependencies
- None explicitly listed (header-only)
- Uses Windows API (not shown in header)
