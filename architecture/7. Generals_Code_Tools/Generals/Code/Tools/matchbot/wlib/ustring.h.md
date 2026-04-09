# Generals/Code/Tools/matchbot/wlib/ustring.h

## Purpose
Defines a templated string class `UstringT` with byte-length constraints, used for internationalized string handling.

## Responsibilities
- Provides a string class with configurable max byte length
- Supports equality comparison for strings
- Manages byte-length limits for character data
- Typedefs `Ustring` for char-based usage

## Key Types
- **UstringT (Class)**: Templated string class with byte-length constraints
- **Ustring (Class)**: Typedef for `UstringT<char>`

## Key Functions
### UstringT/UstringT (constructor)
- Purpose: Initializes with a max character length, converted to bytes
- Calls: `set_max_bytelength`

### UstringT/UstringT (default constructor)
- Purpose: Initializes with default max byte length (4000)
- Calls: None

### UstringT/get_max_bytelength
- Purpose: Returns the current max byte length
- Calls: None

### UstringT/set_max_bytelength
- Purpose: Sets the max byte length
- Calls: None

### UstringT/operator==
- Purpose: Compares two `UstringT` objects for equality
- Calls: None (directly compares underlying `basic_string` objects)

## Globals
- **MAX_BYTES_PER_CHAR (const int)**: Defines bytes per character (1)

## Dependencies
- `<stdlib.h>`, `<stdio.h>`, `<iostream.h>`, `<string>`
- `basic_string`, `string_char_traits` (from `<string>`)
- `size_t` (from `<stdlib.h>`)
