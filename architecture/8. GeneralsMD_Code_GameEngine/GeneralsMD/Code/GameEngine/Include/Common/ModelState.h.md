# GeneralsMD/Code/GameEngine/Include/Common/ModelState.h

## Purpose
Defines the model state system for the game engine, including condition flags and bitmask utilities.

## Responsibilities
- Declares `ModelConditionFlagType` enum for various model states
- Provides `ModelConditionFlags` bitmask type for state combinations
- Defines macros for creating condition masks
- Documents the design rationale for the state system

## Key Types
- `ModelConditionFlagType` (Enum): Enumerates all possible model conditions (e.g., damaged, night, attacking)
- `ModelConditionFlags` (Class): Bitmask wrapper for condition flags
- `MODELCONDITION_INVALID` (Enum): Invalid state marker
- `MODELCONDITION_COUNT` (Enum): Count of valid conditions

## Key Functions
None (header-only file with no function implementations)

## Globals
- `NUM_MODELCONDITION_DOOR_STATES` (const): Defines number of door states (4)

## Dependencies
- `Lib/BaseType.h`
- `Common/INI.h`
- `Common/BitFlags.h`
- `Common/BitFlagsIO.h`
