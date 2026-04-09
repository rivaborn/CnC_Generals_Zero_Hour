# Generals/Code/Tools/Launcher/Toolkit/Support/StringConvert.h

## Purpose
Header file for ANSI <-> Unicode string conversion utilities.

## Responsibilities
- Declares string conversion functions.
- Provides interface for UString class usage.
- Supports character encoding interoperability.

## Key Types
- UString (Class): Unicode string wrapper (forward declaration).

## Key Functions
### UStringToANSI
- Purpose: Converts UString to ANSI-encoded Char buffer.
- Calls: None (declaration only).

### UnicodeToANSI
- Purpose: Converts WChar Unicode string to ANSI-encoded Char buffer.
- Calls: None (declaration only).

## Globals
- None.

## Dependencies
- "UTypes.h" (for Char, WChar, UInt types).
- UString class (forward declared).
