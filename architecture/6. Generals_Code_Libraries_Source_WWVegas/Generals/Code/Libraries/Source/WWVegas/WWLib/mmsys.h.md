# Generals/Code/Libraries/Source/WWVegas/WWLib/mmsys.h

## Purpose
Header file that safely includes the Windows Multimedia System library with specific compiler warning suppression.

## Responsibilities
- Disables warning 4201 for mmsystem.h inclusion
- Provides clean inclusion of Windows multimedia APIs
- Restores warning state after inclusion

## Key Types
- None

## Key Functions
- None

## Globals
- None

## Dependencies
- `<mmsystem.h>`: Windows Multimedia System library
- `_MSC_VER`: Microsoft Visual C++ version check
- `pragma once`: Compiler-specific include guard
