# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/BaseRegenerateUpdate.h

## Purpose
Defines a module for base objects that automatically regenerate health over time.

## Responsibilities
- Implements health regeneration logic for base objects
- Handles damage and healing events
- Provides update functionality for game loop integration
- Manages module data parsing and initialization

## Key Types
- **BaseRegenerateUpdateModuleData (Class)**: Module data container for configuration
- **BaseRegenerateUpdate (Class)**: Main module implementing regeneration and damage handling
- **BaseRegenerateUpdateMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **BaseRegenerateUpdate_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum)

## Key Functions
### BaseRegenerateUpdate::update
- Purpose: Handles periodic health regeneration
- Calls: Not inferable (implementation in .cpp)

### BaseRegenerateUpdate::onDamage
- Purpose: Processes damage events to bases
- Calls: Not inferable (implementation in .cpp)

### BaseRegenerateUpdate::getDisabledTypesToProcess
- Purpose: Returns which disabled states should still process this module
- Calls: None

## Globals
- None

## Dependencies
- `UpdateModule.h` (base class)
- `DamageModule.h` (interface)
- `MultiIniFieldParse` (for module data parsing)
- `Thing` (forward reference)
- `DamageInfo`, `BodyDamageType`, `DisabledMaskType` (external types)
