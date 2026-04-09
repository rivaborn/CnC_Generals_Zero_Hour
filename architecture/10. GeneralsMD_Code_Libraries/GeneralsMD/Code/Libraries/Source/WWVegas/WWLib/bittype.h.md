# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/bittype.h

## Purpose
Defines standard integer and floating-point type aliases for cross-platform consistency.

## Responsibilities
- Provides fixed-size integer types (uint8, uint16, uint32, sint8, sint16, sint32).
- Defines floating-point types (float32, float64).
- Includes common Windows types (DWORD, WORD, BYTE, BOOL, USHORT, LPCSTR, UINT, ULONG).
- Ensures type consistency across different compilers and platforms.

## Key Types
- uint8 (typedef): 8-bit unsigned integer.
- uint16 (typedef): 16-bit unsigned integer.
- uint32 (typedef): 32-bit unsigned integer.
- uint (typedef): Platform-dependent unsigned integer.
- sint8 (typedef): 8-bit signed integer.
- sint16 (typedef): 16-bit signed integer.
- sint32 (typedef): 32-bit signed integer.
- sint (typedef): Platform-dependent signed integer.
- float32 (typedef): 32-bit floating-point number.
- float64 (typedef): 64-bit floating-point number.
- DWORD (typedef): 32-bit unsigned integer (Windows).
- WORD (typedef): 16-bit unsigned integer (Windows).
- BYTE (typedef): 8-bit unsigned integer (Windows).
- BOOL (typedef): Boolean type (Windows).
- USHORT (typedef): 16-bit unsigned integer (Windows).
- LPCSTR (typedef): Null-terminated string pointer (Windows).
- UINT (typedef): 32-bit unsigned integer (Windows).
- ULONG (typedef): 32-bit unsigned integer (Windows).

## Key Functions
None.

## Globals
None.

## Dependencies
- None (header-only file).
