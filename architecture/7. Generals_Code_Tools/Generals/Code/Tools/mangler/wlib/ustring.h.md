# Generals/Code/Tools/mangler/wlib/ustring.h

## Purpose
Defines a templated string class `UstringT` with byte-length constraints, used for internationalized string handling.

## Responsibilities
- Provides a string class with configurable max byte length
- Supports equality comparison for strings
- Manages byte-length limits for character data
- Typedefs `Ustring` for char-based usage

## Key Types
- `UstringT<charT>` (Class): Templated string class with byte-length constraints
- `Ustring` (Typedef): Alias for `UstringT<char>`

## Key Functions
### `UstringT::UstringT(int max_charlength)`
- Purpose: Constructor that sets max byte length based on character length
- Calls: `set_max_bytelength()`

### `UstringT::get_max_bytelength()`
- Purpose: Returns the current max byte length
- Calls: None

### `UstringT::set_max_bytelength(size_t max)`
- Purpose: Sets the max byte length
- Calls: None

### `UstringT::operator==(const UstringT<charT> &other)`
- Purpose: Compares two UstringT objects for equality
- Calls: None (uses inherited `operator==`)

## Globals
- `MAX_BYTES_PER_CHAR` (const int): Defines bytes per character (1)

## Dependencies
- `<stdlib.h>`, `<stdio.h>`, `<iostream.h>`, `<string>`
- `basic_string`, `string_char_traits` (from `<string>`)
