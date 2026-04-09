# Generals/Code/Tools/Launcher/Toolkit/Support/StringConvert.cpp

## Purpose
Provides functions for converting Unicode strings to ANSI strings.

## Responsibilities
- Convert Unicode strings to ANSI strings
- Handle buffer management for string conversions
- Provide wrapper functions for string conversion utilities

## Key Types
- None

## Key Functions
### UStringToANSI
- Purpose: Converts a UString to an ANSI string
- Calls: UnicodeToANSI

### UnicodeToANSI
- Purpose: Converts a Unicode string to an ANSI string
- Calls: WideCharToMultiByte (Windows API)

## Globals
- None

## Dependencies
- StringConvert.h
- UString.h
- windows.h (for WideCharToMultiByte)
- Debug\DebugPrint.h (for PrintWin32Error)
- assert.h (for assert)
