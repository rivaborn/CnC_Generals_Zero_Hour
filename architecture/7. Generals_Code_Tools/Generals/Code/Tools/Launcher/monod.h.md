# Generals/Code/Tools/Launcher/monod.h

## Purpose
Header file defining the MonoD class for monochrome display output, primarily for Windows.

## Responsibilities
- Declares MonoD class inheriting from OutputDevice
- Defines IOCTL codes for monochrome display control (Windows-only)
- Provides interface for text output to monochrome display

## Key Types
- MonoD (Class): Monochrome display output device wrapper

## Key Functions
### MonoD()
- Purpose: Constructor for MonoD class
- Calls: Not inferable

### ~MonoD()
- Purpose: Destructor for MonoD class
- Calls: Not inferable

### print(const char *str, int len)
- Purpose: Outputs text to monochrome display
- Calls: Not inferable

## Globals
None

## Dependencies
- stdlib.h, stdio.h
- odevice.h (OutputDevice base class)
- Windows.h, winioctl.h (Windows-only)
