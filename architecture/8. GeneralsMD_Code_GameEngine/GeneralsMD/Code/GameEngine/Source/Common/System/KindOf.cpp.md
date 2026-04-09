# GeneralsMD/Code/GameEngine/Source/Common/System/KindOf.cpp

## Purpose
Initializes and defines bitmask flags for game object types in the SAGE engine.

## Responsibilities
- Defines bitmask flag names for object types
- Initializes `KINDOFMASK_FS` with faction-specific building types
- Provides lookup table for debugging flag names

## Key Types
- `KindOfMaskType` (Class): Bitmask wrapper for object type flags
- `KINDOFMASK_NONE` (KindOfMaskType): Empty mask
- `KINDOFMASK_FS` (KindOfMaskType): Mask for faction-specific structures

## Key Functions
### `initKindOfMasks`
- Purpose: Initializes faction-specific building type mask
- Calls: `KindOfMaskType::set` (17 times)

## Globals
- `s_bitNameList` (const char*): Array of flag name strings
- `KINDOFMASK_NONE` (KindOfMaskType): Zero-initialized mask
- `KINDOFMASK_FS` (KindOfMaskType): Zero-initialized mask

## Dependencies
- `Common/KindOf.h`
- `Common/BitFlagsIO.h`
- `PreRTS.h`
