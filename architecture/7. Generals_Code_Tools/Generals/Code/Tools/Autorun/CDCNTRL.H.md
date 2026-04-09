# Generals/Code/Tools/Autorun/CDCNTRL.H

## Purpose
Header file defining a CD control class for managing CD-ROM drive operations (ejecting, locking/unlocking trays) on Windows systems.

## Responsibilities
- Provides cross-platform CD-ROM control functionality
- Manages CD tray locking/unlocking
- Handles platform-specific CD operations (NT vs Win9x)
- Exposes high-level CD control API

## Key Types
- **CDControlClass (Class)**: Main class for CD-ROM control operations
- **DIOC_REGISTERS (Struct)**: Low-level DOS IOCTL register structure
- **PARAMBLOCK (Struct)**: Parameters for locking/unlocking removable media

## Key Functions
### Force_CD_Eject
- Purpose: Forces CD tray ejection on specified drive
- Calls: Eject_CD, Eject_CD_Win95

### Lock_CD_Tray
- Purpose: Prevents CD tray ejection on specified drive
- Calls: Lock_CD_Drive, Lock_CD_Drive_95

### Unlock_CD_Tray
- Purpose: Allows CD tray ejection on specified drive
- Calls: Unlock_CD_Drive, Unlock_CD_Drive_95

## Globals
- **CDControl (CDControlClass)**: Global instance of CD control class
- **LOCK_TIMEOUT (const)**: Timeout value for locking operations (2000ms)
- **LOCK_RETRIES (const)**: Number of retry attempts for locking (2)

## Dependencies
- Windows.h, Windowsx.h, ctype.h
- Platform-specific CD-ROM control APIs
- DOS IOCTL infrastructure for Win9x support
