# GeneralsMD/Code/GameEngine/Source/Common/BitFlags.cpp

## Purpose
Defines and initializes bit flag enums for game state tracking, particularly for model conditions and armor sets.

## Responsibilities
- Initializes string names for ModelConditionFlags bit flags
- Initializes string names for ArmorSetFlags bit flags
- Provides human-readable names for bitmask debugging

## Key Types
- ModelConditionFlags (enum): Tracks various model states (e.g., damaged, firing, constructing)
- ArmorSetFlags (enum): Tracks armor/unit upgrade states (e.g., veteran, elite, hero)

## Key Functions
None (file only contains global data initialization)

## Globals
- ModelConditionFlags::s_bitNameList (const char*): Array of strings mapping ModelConditionFlags to names
- ArmorSetFlags::s_bitNameList (const char*): Array of strings mapping ArmorSetFlags to names

## Dependencies
- "Common/BitFlags.h" (header for flag enums)
- "Common/BitFlagsIO.h" (I/O utilities for flags)
- "Common/ModelState.h" (model state definitions)
- "GameLogic/ArmorSet.h" (armor set definitions)
