# Generals/Code/Tools/matchbot/wlib/monod.h

## Purpose
Defines the MonoD class for monochrome display output, primarily for Windows.

## Responsibilities
- Provides monochrome display output functionality
- Handles IOCTL commands for monochrome display control
- Manages display device handle (Windows-specific)
- Implements basic text printing

## Key Types
- MonoD (Class): Monochrome display output device wrapper

## Key Functions
### MonoD::MonoD
- Purpose: Constructor for MonoD class
- Calls: None

### MonoD::~MonoD
- Purpose: Destructor for MonoD class
- Calls: None

### MonoD::print
- Purpose: Prints text to the monochrome display
- Calls: None

## Globals
- None

## Dependencies
- `<stdlib.h>`
- `<stdio.h>`
- `"odevice.h"`
- Windows-specific headers (`<windows.h>`, `<winioctl.h>`) when `_WIN32` is defined
- OutputDevice (base class)
