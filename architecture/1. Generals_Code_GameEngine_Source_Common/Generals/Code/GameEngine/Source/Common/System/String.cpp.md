# Generals/Code/GameEngine/Source/Common/System/String.cpp

## Purpose
This file implements a custom string class `WSYS_String` for handling strings in the Command & Conquer Generals game engine, providing functionalities like concatenation, comparison, and formatting.

## Responsibilities
- Implementing basic string operations such as assignment, concatenation, and comparison.
- Providing methods for string manipulation like making strings uppercase or lowercase.
- Handling dynamic memory allocation and deallocation for string data.

## Key Types
- `WSYS_String (Class)`: A custom string class with methods for various string operations.

## Key Functions
### WSYS_String::operator+= 
- Purpose: Concatenates another string to the current string.
- Calls: `MSGNEW`, `strcpy`, `strcat`, `delete[]`

### operator+ (const WSYS_String &string1, const WSYS_String &string2)
- Purpose: Overloads the + operator to concatenate two strings.
- Calls: `WSYS_String::operator+=`

### operator+ (const Char *string1, const WSYS_String &string2)
- Purpose: Overloads the + operator to concatenate a C-style string and a `WSYS_String`.
- Calls: `WSYS_String::operator+=`

### operator+ (const WSYS_String &string1, const Char *string2)
- Purpose: Overloads the + operator to concatenate a `WSYS_String` and a C-style string.
- Calls: `WSYS_String::operator+=`

## Globals
- None

## Dependencies
- Includes: `<stdio.h>`, `<stdlib.h>`, `<stdarg.h>`, `<string.h>`
- External symbols used: `strcmp`, `strcpy`, `strcat`, `strlen`, `toupper`, `tolower`
