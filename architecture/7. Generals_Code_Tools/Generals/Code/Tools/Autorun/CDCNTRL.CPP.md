# Generals/Code/Tools/Autorun/CDCNTRL.CPP

## Purpose
Manages CD/DVD drive control operations including locking, unlocking, and ejecting media for Windows 9x and NT platforms.

## Responsibilities
- Provides platform-specific CD control functions
- Handles volume locking/unlocking and media ejection
- Manages VWIN32 device handle operations for Win9x
- Implements error reporting for CD control operations

## Key Types
- CDControlClass (Class): Main class for CD control operations
- DIOC_REGISTERS (Struct): Register structure for DOS IO control
- PARAMBLOCK (Struct): Parameter block for DOS IO control operations

## Key Functions
### Force_CD_Eject
- Purpose: Ejects CD tray on specified drive
- Calls: Eject_CD_Win95 or Eject_CD based on OS version

### Lock_CD_Tray
- Purpose: Prevents CD ejection on specified drive
- Calls: Lock_CD_Drive_95 or Lock_CD_Drive based on OS version

### Open_Removable_Volume
- Purpose: Opens handle to removable volume
- Calls: GetDriveType, CreateFile

### Lock_Volume
- Purpose: Locks volume to prevent access by other threads
- Calls: DeviceIoControl with FSCTL_LOCK_VOLUME

### Auto_Eject_Volume
- Purpose: Ejects removable media
- Calls: DeviceIoControl with IOCTL_STORAGE_EJECT_MEDIA

### Open_VWin32
- Purpose: Opens handle to VWIN32 device for low-level disk I/O
- Calls: CreateFile

### Lock_Logical_Volume
- Purpose: Takes lock on logical volume for Win9x
- Calls: DeviceIoControl with VWIN32_DIOC_DOS_IOCTL

## Globals
- CDControl (CDControlClass): Global instance of CD control class

## Dependencies
- winioctl.h, tchar.h, stdio.h
- CDCNTRL.H, WINFIX.H, WND_FILE.H
- WinVersion class for OS detection
- Msg() function for error reporting
- DeviceIoControl API for volume control operations
