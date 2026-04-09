# GeneralsMD/Code/GameEngine/Include/Precompiled/PreRTS.h

## Purpose
Precompiled header file that includes frequently used headers to speed up compilation.

## Responsibilities
- Includes system headers (Windows API, C runtime, etc.)
- Includes STL-related headers (via STLTypedefs)
- Includes core game engine headers (Basetype, GameCommon, etc.)
- Defines custom STL allocator (STLSpecialAlloc)
- Centralizes common dependencies to avoid duplication

## Key Types
- STLSpecialAlloc (Class): Custom STL allocator for memory management

## Key Functions
None

## Globals
None

## Dependencies
- System headers: windows.h, stdlib.h, string.h, etc.
- STL headers: (indirectly via STLTypedefs)
- Game engine headers: Basetype.h, GameCommon.h, INI.h, KindOf.h
- DirectInput headers: dinput.h
- External symbols: _STLP_USE_NEWALLOC, _STLP_USE_CUSTOM_NEWALLOC
