# Generals/Code/GameEngine/Source/Common/System/QuotedPrintable.cpp

## Purpose
This file contains functions for encoding and decoding strings using the Quoted-Printable format, which is used to encode binary data in ASCII text.

## Responsibilities
- Convert Unicode and ASCII strings to Quoted-Printable format.
- Convert Quoted-Printable encoded strings back to Unicode and ASCII.

## Key Types
- None

## Key Functions
### intToHexDigit
- Purpose: Converts an integer to its corresponding hexadecimal digit character.
- Calls: None

### hexDigitToInt
- Purpose: Converts a hexadecimal digit character to its corresponding integer value.
- Calls: None

### UnicodeStringToQuotedPrintable
- Purpose: Encodes a Unicode string into Quoted-Printable format.
- Calls: intToHexDigit

### AsciiStringToQuotedPrintable
- Purpose: Encodes an ASCII string into Quoted-Printable format.
- Calls: intToHexDigit

### QuotedPrintableToUnicodeString
- Purpose: Decodes a Quoted-Printable encoded string back to a Unicode string.
- Calls: hexDigitToInt

### QuotedPrintableToAsciiString
- Purpose: Decodes a Quoted-Printable encoded string back to an ASCII string.
- Calls: hexDigitToInt

## Globals
- MAGIC_CHAR (char): Used as a marker for encoded characters.

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/QuotedPrintable.h"
