# Generals/Code/Tools/mangler/wlib/monod.h

## Purpose
Defines a monochrome display driver class for Windows, handling text output via IOCTL commands.

## Responsibilities
- Encapsulates monochrome display device operations
- Provides text printing functionality
- Manages Windows-specific device handle
- Implements IOCTL-based control commands

## Key Types
- **MonoD (Class)**: Monochrome display driver interface

## Key Functions
### MonoD::MonoD
- Purpose: Constructor for MonoD class
- Calls: None

### MonoD::~MonoD
- Purpose: Destructor for MonoD class
- Calls: None

### MonoD::print
- Purpose: Prints a string to the monochrome display
- Calls: None

## Globals
- **FILE_DEVICE_MONO (int)**: Device type identifier
- **IOCTL_MONO_* (int)**: IOCTL command codes for various operations

## Dependencies
- `<stdlib.h>`, `<stdio.h>`
- `"odevice.h"` (OutputDevice base class)
- Windows-specific headers (`<windows.h>`, `<winioctl.h>`) when `_WIN32` is defined
