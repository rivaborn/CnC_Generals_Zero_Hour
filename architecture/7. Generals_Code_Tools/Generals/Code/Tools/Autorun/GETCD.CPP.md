# Generals/Code/Tools/Autorun/GETCD.CPP

## Purpose
Handles CD-ROM drive detection and volume label verification for game installation/autorun.

## Responsibilities
- Detect available CD-ROM drives
- Verify CD volume labels against expected game labels
- Provide CD drive information to other tools

## Key Types
- `GetCDClass` (Class): Manages CD drive detection and volume label operations
- `_CD_Volume_Label` (Array): Expected CD volume labels for game verification

## Key Functions
### `GetCDClass::Get_CD_Drive_For_This_Volume`
- Purpose: Finds CD drive containing specified volume label
- Calls: `GetVolumeInformation`, `WinVersion.Is_Win95`

### `CD_Volume_Verification`
- Purpose: Verifies CD volume label matches expected game label
- Calls: `GetVolumeInformation`, `WinVersion.Is_Win95`

## Globals
- `_CD_Volume_Label` (char*): Expected CD volume labels
- `_Num_Volumes` (int): Number of expected volume labels
- `CDList` (GetCDClass): Global CD drive manager instance

## Dependencies
- Windows API (`windows.h`)
- `getcd.h` (header for CD operations)
- `wnd_file.h` (for message logging)
- `winfix.h` (for Windows version detection)
