# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/MONODRVR.H

## Purpose
Header file defining IOCTL codes and structures for a monochrome display driver interface.

## Responsibilities
- Defines device-specific IOCTL codes for monochrome display control
- Declares MonoFlagType enum for driver behavior flags
- Provides example usage of the driver interface
- Includes Windows-specific headers for IOCTL support

## Key Types
- **MonoFlagType (enum)**: Monochrome display driver behavior flags (e.g., text wrapping)

## Key Functions
None (header-only file)

## Globals
- **FILE_DEVICE_MONO (macro)**: Device type identifier (0x00008000)
- **IOCTL_MONO_* (macros)**: IOCTL control codes for various display operations

## Dependencies
- `<winioctl.h>` (Windows IOCTL definitions)
- `CreateFile`, `WriteFile`, `DeviceIoControl`, `CloseHandle` (Windows API functions)
- `HANDLE`, `DWORD` (Windows types)
