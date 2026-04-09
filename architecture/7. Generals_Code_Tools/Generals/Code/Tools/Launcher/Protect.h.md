# Generals/Code/Tools/Launcher/Protect.h

## Purpose
Header file for copy protection mechanisms in the game launcher.

## Responsibilities
- Defines copy protection interface
- Provides platform-specific implementations (Windows)
- Manages process synchronization and secure communication

## Key Types
- `Protect` (Class): Main copy protection handler (old implementation)
- `RefPtr` (Template): Reference-counted pointer (forward declaration)
- `UString` (Class): Unicode string wrapper (forward declaration)

## Key Functions
### `InitializeProtect`
- Purpose: Initialize copy protection system
- Calls: Not inferable

### `ShutdownProtect`
- Purpose: Clean up copy protection resources
- Calls: Not inferable

### `SendProtectMessage`
- Purpose: Send protection data to another process
- Calls: Not inferable

### `SendMappedFileHandle`
- Purpose: Share mapped file handle with another process
- Calls: Not inferable

### `GetPassKey`
- Purpose: Retrieve machine-specific authentication key
- Calls: Not inferable

## Globals
- `mLauncherMutex` (HANDLE): Mutex for launcher synchronization
- `mMappedFile` (HANDLE): Handle to shared memory mapping

## Dependencies
- `<windows.h>`: Windows API headers
- `RefPtr`, `UString`: Internal string/pointer utilities
- `HANDLE`, `DWORD`: Windows data types
