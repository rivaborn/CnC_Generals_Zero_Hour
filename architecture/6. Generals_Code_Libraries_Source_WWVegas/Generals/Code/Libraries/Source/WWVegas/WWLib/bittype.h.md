# Generals/Code/Libraries/Source/WWVegas/WWLib/bittype.h

## Purpose
Defines standard integer and floating-point type aliases for cross-platform consistency.

## Responsibilities
- Provides fixed-size integer types (uint8, uint16, uint32, sint8, sint16, sint32).
- Defines floating-point types (float32, float64).
- Includes Windows-specific types (DWORD, WORD, BYTE, BOOL, USHORT, LPCSTR, UINT, ULONG).

## Key Types
- uint8 (typedef): 8-bit unsigned integer.
- uint16 (typedef): 16-bit unsigned integer.
- uint32 (typedef): 32-bit unsigned integer.
- uint (typedef): Platform-dependent unsigned integer.
- sint8 (typedef): 8-bit signed integer.
- sint16 (typedef): 16-bit signed integer.
- sint32 (typedef): 32-bit signed integer.
- sint (typedef): Platform-dependent signed integer.
- float32 (typedef): 32-bit floating-point.
- float64 (typedef): 64-bit floating-point.
- DWORD (typedef): Windows DWORD (32-bit unsigned).
- WORD (typedef): Windows WORD (16-bit unsigned).
- BYTE (typedef): Windows BYTE (8-bit unsigned).
- BOOL (typedef): Windows BOOL (int).
- USHORT (typedef): Windows USHORT (16-bit unsigned).
- LPCSTR (typedef): Windows LPCSTR (const char*).
- UINT (typedef): Windows UINT (32-bit unsigned).
- ULONG (typedef): Windows ULONG (32-bit unsigned).

## Key Functions
None.

## Globals
None.

## Dependencies
- None (header-only).
