# Generals/Code/Tools/Babylon/olestring.cpp

## Purpose
Implements string manipulation utilities for OLEString class, handling Unicode/ANSI conversions and format string processing.

## Responsibilities
- Manages OLEString class lifecycle (construction/destruction)
- Provides string formatting and meta-character conversion
- Handles space stripping and format string comparison
- Supports Unicode/ANSI string interconversion

## Key Types
- OLEString (Class): Wrapper for Unicode/ANSI string pairs with formatting support
- format_type (char*): Static string defining valid printf format types

## Key Functions
### IsFormatTypeChar
- Purpose: Checks if character is a valid printf format type
- Calls: None

### StripSpaces
- Purpose: Removes consecutive spaces from strings
- Calls: None

### StripSpacesFromMetaString
- Purpose: Strips spaces while preserving escape sequences
- Calls: None

### ConvertMetaChars
- Purpose: Converts escape sequences (\n, \t) to actual characters
- Calls: None

### SameFormat
- Purpose: Compares two format strings ignoring non-format content
- Calls: IsFormatTypeChar

### EncodeFormat/DecodeFormat
- Purpose: Placeholder functions for format encoding/decoding
- Calls: None

## Globals
- format_type (char*): String containing valid printf format characters

## Dependencies
- stdAfx.h, assert.h, olestring.h
- Uses wcscpy, wcslen, sprintf, swprintf, strlen, strcpy, wcslen
- Depends on OLECHAR and char types
