# Generals/Code/Tools/mangler/wlib/monod.cpp

## Purpose
Handles low-level console output via Windows device driver or stderr fallback.

## Responsibilities
- Initializes connection to MONO device driver on Windows
- Provides cross-platform text output method
- Clears screen on initialization (Windows only)
- Manages handle lifecycle for MONO device

## Key Types
- `MonoD` (Class): Console output wrapper for MONO device driver

## Key Functions
### `MonoD::MonoD()`
- Purpose: Constructor initializes MONO device handle and clears screen
- Calls: `CreateFile`, `DeviceIoControl`

### `MonoD::~MonoD()`
- Purpose: Destructor cleans up MONO device handle
- Calls: `CloseHandle`

### `MonoD::print()`
- Purpose: Outputs text to MONO device or stderr
- Calls: `WriteFile` (Windows), `fprintf` (non-Windows)

## Globals
- `handle` (HANDLE): Stores Windows device handle (Windows only)

## Dependencies
- Windows API: `CreateFile`, `CloseHandle`, `WriteFile`, `DeviceIoControl`
- C runtime: `fprintf`
- Custom: `IOCTL_MONO_CLEAR_SCREEN` (Windows IO control code)
