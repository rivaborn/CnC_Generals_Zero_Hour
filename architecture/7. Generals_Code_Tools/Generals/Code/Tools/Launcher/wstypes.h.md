# Generals/Code/Tools/Launcher/wstypes.h

## Purpose
Defines standard type aliases and macros for portability and readability in the SAGE engine.

## Responsibilities
- Provides fixed-width integer types (bit8, sint8, uint8, sint16, uint16, sint32, uint32).
- Defines common macros (TRUE, FALSE, MIN, MAX, NULL, IN, OUT, INOUT).
- Sets max values for integer types.
- Handles platform-specific string comparisons (_WIN32).

## Key Types
- bit8 (typedef): 8-bit signed integer (char).
- sint8 (typedef): 8-bit signed integer (char).
- uint8 (typedef): 8-bit unsigned integer (unsigned char).
- sint16 (typedef): 16-bit signed integer (signed short int).
- uint16 (typedef): 16-bit unsigned integer (unsigned short int).
- sint32 (typedef): 32-bit signed integer (signed int).
- uint32 (typedef): 32-bit unsigned integer (unsigned int).

## Key Functions
None.

## Globals
- MAX_BIT8 (const): Max value for bit8 (0x1).
- MAX_UINT32 (const): Max value for uint32 (0xFFFFFFFF).
- MAX_UINT16 (const): Max value for uint16 (0xFFFF).
- MAX_UINT8 (const): Max value for uint8 (0xFF).
- MAX_SINT32 (const): Max value for sint32 (0x7FFFFFFF).
- MAX_SINT16 (const): Max value for sint16 (0x7FFF).
- MAX_SINT8 (const): Max value for sint8 (0x7F).

## Dependencies
- Platform-specific macros (_WIN32 for string comparisons).
