# Generals/Code/Tools/matchbot/wlib/monod.cpp

## Purpose
Handles low-level console output via a Windows device driver or stderr fallback.

## Responsibilities
- Initializes and cleans up a handle to the MONO device driver on Windows.
- Provides cross-platform text output (Windows via device driver, others via stderr).
- Manages device I/O control for screen clearing.

## Key Types
- `MonoD` (Class): Wrapper for MONO device driver interaction.

## Key Functions
### `MonoD::MonoD()`
- Purpose: Constructor initializes the MONO device handle and clears the screen.
- Calls: `CreateFile`, `DeviceIoControl`.

### `MonoD::~MonoD()`
- Purpose: Destructor closes the MONO device handle.
- Calls: `CloseHandle`.

### `MonoD::print(const char *str, int len)`
- Purpose: Writes text to the MONO device or stderr.
- Calls: `WriteFile` (Windows), `fprintf` (non-Windows).

## Globals
- `handle` (HANDLE): Stores the Windows device handle.

## Dependencies
- Windows API: `CreateFile`, `CloseHandle`, `WriteFile`, `DeviceIoControl`.
- C runtime: `fprintf`.
- Custom: `IOCTL_MONO_CLEAR_SCREEN`, `IOCTL_MONO_PRINT_RAW`.
