# Generals/Code/Tools/Babylon/olestring.h

## Purpose
Header file defining the OLEString class and related string manipulation utilities for handling OLECHAR and char strings.

## Responsibilities
- Define OLEString class for managing OLECHAR and char string pairs
- Provide string manipulation functions (stripping spaces, meta-char conversion, format encoding/decoding)
- Support template-based string operations for type safety

## Key Types
- OLEString (Class): Wrapper for OLECHAR and char string pairs with utility methods

## Key Functions
### StripSpaces
- Purpose: Remove spaces from a string
- Calls: Not inferable

### ConvertMetaChars
- Purpose: Convert meta-characters in a string
- Calls: Not inferable

### StripSpacesFromMetaString
- Purpose: Remove spaces from a meta-string
- Calls: Not inferable

### SameFormat
- Purpose: Check if two strings have the same format
- Calls: Not inferable

### EncodeFormat
- Purpose: Encode format characters in a string
- Calls: Not inferable

### DecodeFormat
- Purpose: Decode format characters in a string
- Calls: Not inferable

### IsFormatTypeChar
- Purpose: Check if a character is a format type character
- Calls: Not inferable

## Globals
- OLESTRING_DEFAULT_SIZE (unsigned int): Default size for OLEString buffers

## Dependencies
- Uses OLECHAR and OLESTRING types (Windows OLE)
- Uses char for string buffers
- Uses TRUE/FALSE constants (Windows)
- No external includes visible in header
