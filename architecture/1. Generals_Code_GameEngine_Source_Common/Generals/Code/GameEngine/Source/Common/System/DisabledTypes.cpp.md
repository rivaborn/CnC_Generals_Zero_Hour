# Generals/Code/GameEngine/Source/Common/System/DisabledTypes.cpp

## Purpose
This file initializes and defines disabled mask types used in the game engine to manage various states of units or objects that are disabled for different reasons.

## Responsibilities
- Defines constants for disabled masks.
- Initializes global disabled mask variables.
- Provides a function to set all bits in a disabled mask.

## Key Types
- `DisabledMaskType` (struct): Represents different types of disablement flags.

## Key Functions
### initDisabledMasks
- Purpose: Initializes the `DISABLEDMASK_ALL` variable with all bits set.
- Calls: `SET_ALL_DISABLEDMASK_BITS`

## Globals
- `DISABLEDMASK_NONE` (`DisabledMaskType`): Represents no disabled states.
- `DISABLEDMASK_ALL` (`DisabledMaskType`): Represents all possible disabled states.

## Dependencies
- Key includes:
  - `"Common/DisabledTypes.h"`
  - `"Common/BitFlagsIO.h"`

- External symbols used but not defined here:
  - `SET_ALL_DISABLEDMASK_BITS`
  - `DisabledMaskType::s_bitNameList`
