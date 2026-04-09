# GeneralsMD/Code/GameEngine/Source/Common/System/ObjectStatusTypes.cpp

## Purpose
Defines object status types and their string representations for bitmask operations in the game engine.

## Responsibilities
- Declares and initializes the `OBJECT_STATUS_MASK_NONE` global variable.
- Provides human-readable names for each status bit via `s_bitNameList`.
- Supports serialization/deserialization of status flags (via `BitFlagsIO.h`).

## Key Types
- `ObjectStatusMaskType` (class): Bitmask container for object status flags.
- `s_bitNameList` (const char*): Array of status flag names for debugging/output.

## Key Functions
### None
- No functions defined in this file.

## Globals
- `OBJECT_STATUS_MASK_NONE` (ObjectStatusMaskType): Zero-initialized status mask.

## Dependencies
- `Common/ObjectStatusTypes.h`: Header for `ObjectStatusMaskType`.
- `Common/BitFlagsIO.h`: For bitmask I/O utilities.
- `PreRTS.h`: Likely engine precompiled header.
