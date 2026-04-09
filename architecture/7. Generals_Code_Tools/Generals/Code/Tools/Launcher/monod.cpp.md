# Generals/Code/Tools/Launcher/monod.cpp

## Purpose
Implements a cross-platform mono display driver for the launcher tool.

## Responsibilities
- Manages a handle to the MONO device on Windows
- Provides text output via `print()` for both Windows and non-Windows platforms
- Clears the screen on initialization (Windows only)
- Handles resource cleanup in destructor

## Key Types
- `MonoD` (Class): Mono display driver wrapper

## Key Functions
### `MonoD::MonoD()`
- Purpose: Constructor that initializes the MONO device handle and clears the screen on Windows.
- Calls: `CreateFile`, `DeviceIoControl`

### `MonoD::~MonoD()`
- Purpose: Destructor that closes the MONO device handle on Windows.
- Calls: `CloseHandle`

### `MonoD::print(const char *str, int len)`
- Purpose: Outputs text to the mono display, using `WriteFile` on Windows or `fprintf` on other platforms.
- Calls: `WriteFile`, `fprintf`

## Globals
- `handle` (HANDLE): Stores the Windows device handle for MONO device access

## Dependencies
- Windows API: `CreateFile`, `CloseHandle`, `WriteFile`, `DeviceIoControl`, `GENERIC_READ`, `GENERIC_WRITE`, `OPEN_EXISTING`, `FILE_ATTRIBUTE_NORMAL`, `INVALID_HANDLE_VALUE`
- C runtime: `fprintf`, `stderr`
- Custom: `IOCTL_MONO_CLEAR_SCREEN` (not defined in this file)
