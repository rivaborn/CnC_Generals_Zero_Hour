# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/AnimationSteeringUpdate.h

## Purpose
Defines a game logic module that handles steering behavior using animation states.

## Responsibilities
- Manages animation-based steering transitions
- Controls timing for animation state changes
- Integrates with the game's update module system
- Parses configuration data for steering parameters

## Key Types
- **PhysicsTurningType (Enum)**: Not inferable.
- **AnimationSteeringUpdateModuleData (Class)**: Holds configuration data for steering transitions.
- **AnimationSteeringUpdate (Class)**: Implements the steering update logic.
- **AnimationSteeringUpdateMagicEnum (Enum)**: Not inferable.
- **AnimationSteeringUpdate_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable.

## Key Functions
### AnimationSteeringUpdateModuleData::buildFieldParse
- Purpose: Registers INI field parsing for module data.
- Calls: `UpdateModuleData::buildFieldParse`

### AnimationSteeringUpdate::update
- Purpose: Executes the steering update logic.
- Calls: Not inferable.

## Globals
- None

## Dependencies
- `UpdateModule.h`
- `MultiIniFieldParse`
- `INI` namespace
- `Thing` class
- `ModuleData` class
- `ModelConditionFlagType` type
