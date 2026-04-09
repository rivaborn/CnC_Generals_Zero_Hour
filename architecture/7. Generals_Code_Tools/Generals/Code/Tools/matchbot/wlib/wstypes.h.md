# Generals/Code/Tools/matchbot/wlib/wstypes.h

## Purpose
Defines standard type aliases and macros for portability and readability in the matchbot tool.

## Responsibilities
- Provides cross-platform type definitions (bit8, sint8, uint8, etc.)
- Defines common macros (TRUE, FALSE, MIN, MAX, NULL)
- Handles thread-safe includes and platform-specific adjustments
- Declares input/output parameter macros (IN, OUT, INOUT)
- Defines string comparison macros for Windows compatibility

## Key Types
- bit8 (typedef): 8-bit signed integer
- sint8 (typedef): 8-bit signed integer
- uint8 (typedef): 8-bit unsigned integer
- sint16 (typedef): 16-bit signed integer
- uint16 (typedef): 16-bit unsigned integer
- sint32 (typedef): 32-bit signed integer
- uint32 (typedef): 32-bit unsigned integer
- float32 (typedef): 32-bit floating point
- float64 (typedef): 64-bit floating point

## Key Functions
None

## Globals
- MAX_BIT8 (const): Maximum value for bit8 (0x1)
- MAX_UINT32 (const): Maximum value for uint32 (0xFFFFFFFF)
- MAX_UINT16 (const): Maximum value for uint16 (0xFFFF)
- MAX_UINT8 (const): Maximum value for uint8 (0xFF)
- MAX_SINT32 (const): Maximum value for sint32 (0x7FFFFFFF)
- MAX_SINT16 (const): Maximum value for sint16 (0x7FFF)
- MAX_SINT8 (const): Maximum value for sint8 (0x7F)

## Dependencies
- `<time.h>`, `<stdlib.h>`, `<stdio.h>
