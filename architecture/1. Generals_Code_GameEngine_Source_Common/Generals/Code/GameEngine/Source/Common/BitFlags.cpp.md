# Generals/Code/GameEngine/Source/Common/BitFlags.cpp

## Purpose
This file defines and initializes bit flag arrays for model conditions and armor sets, used to manage various states of game entities.

## Responsibilities
- Define and initialize bit flag arrays for model conditions.
- Define and initialize bit flag arrays for armor sets.

## Key Types
- `ModelConditionFlags` (struct): Contains a list of bit names representing different model conditions.
- `ArmorSetFlags` (struct): Contains a list of bit names representing different armor set levels.

## Key Functions
None

## Globals
- `s_bitNameList` (const char*[]): Array of strings defining bit flag names for model conditions.
- `s_bitNameList` (const char*[]): Array of strings defining bit flag names for armor sets.

## Dependencies
- Includes: "PreRTS.h", "Common/BitFlags.h", "Common/BitFlagsIO.h", "Common/ModelState.h", "GameLogic/ArmorSet.h"
- External symbols: None
