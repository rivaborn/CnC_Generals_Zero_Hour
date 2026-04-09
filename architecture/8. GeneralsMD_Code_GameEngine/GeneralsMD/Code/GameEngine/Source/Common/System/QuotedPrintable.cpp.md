# GeneralsMD/Code/GameEngine/Source/Common/System/QuotedPrintable.cpp

## Purpose
Implements quoted-printable encoding and decoding for ASCII and Unicode strings.

## Responsibilities
- Converts Unicode strings to quoted-printable ASCII
- Converts ASCII strings to quoted-printable format
- Decodes quoted-printable strings back to Unicode or ASCII
- Handles hex digit conversions for encoding/decoding

## Key Types
- None

## Key Functions
### intToHexDigit
- Purpose: Converts an integer (0-15) to its hex digit character representation
- Calls: None

### hexDigitToInt
- Purpose: Converts a hex digit character to its integer value
- Calls: None

### UnicodeStringToQuotedPrintable
- Purpose: Encodes a Unicode string into quoted-printable ASCII format
- Calls: intToHexDigit, isalnum

### AsciiStringToQuotedPrintable
- Purpose: Encodes an ASCII string into quoted-printable format
- Calls: intToHexDigit, isalnum

### QuotedPrintableToUnicodeString
- Purpose: Decodes a quoted-printable string back into a Unicode string
- Calls: hexDigitToInt

### QuotedPrintableToAsciiString
- Purpose: Decodes a quoted-printable string back into an ASCII string
- Calls: hexDigitToInt

## Globals
- MAGIC_CHAR (const char): The character used to denote encoded sequences ('_')

## Dependencies
- "Common/QuotedPrintable.h" (header)
- "PreRTS.h" (project-specific include)
- isalnum (C library function)
