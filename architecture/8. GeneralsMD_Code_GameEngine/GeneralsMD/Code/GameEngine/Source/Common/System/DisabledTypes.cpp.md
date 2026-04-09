# GeneralsMD/Code/GameEngine/Source/Common/System/DisabledTypes.cpp

## Purpose
Initializes and defines disabled state bitmasks for game entities.

## Responsibilities
- Defines bitmask constants for disabled states
- Initializes global disabled mask variables
- Provides bitmask type names for serialization

## Key Types
- DisabledMaskType (struct): bitmask for disabled states
- s_bitNameList (array): string names for disabled state bits

## Key Functions
### initDisabledMasks
- Purpose: Initializes the ALL disabled mask to include all bits
- Calls: SET_ALL_DISABLEDMASK_BITS

## Globals
- DISABLEDMASK_NONE (DisabledMaskType): Zero-initialized mask
- DISABLEDMASK_ALL (DisabledMaskType): Mask with all bits set
- s_bitNameList (const char*): Array of disabled state names

## Dependencies
- "Common/DisabledTypes.h"
- "Common/BitFlagsIO.h"
- SET_ALL_DISABLEDMASK_BITS macro
