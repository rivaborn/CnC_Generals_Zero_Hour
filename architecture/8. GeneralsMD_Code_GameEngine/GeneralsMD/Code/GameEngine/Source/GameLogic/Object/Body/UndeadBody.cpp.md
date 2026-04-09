# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Body/UndeadBody.cpp

## Purpose
Implements the UndeadBody module, which handles a two-phase death system for game objects.

## Responsibilities
- Intercepts first death to trigger "second life" with modified health/armor
- Manages damage logic to prevent instant death on first hit
- Coordinates slow death behavior activation after first death
- Serializes module state for network sync

## Key Types
- **UndeadBodyModuleData (struct)**: Stores second-life max health value
- **UndeadBody (class)**: Extends ActiveBody to implement undead behavior

## Key Functions
### `buildFieldParse`
- Purpose: Registers INI field parsing for UndeadBodyModuleData
- Calls: `ActiveBodyModuleData::buildFieldParse`

### `attemptDamage`
- Purpose: Handles damage with special logic for first death interception
- Calls: `ActiveBody::attemptDamage`, `startSecondLife`, `IsHealthDamagingDamage`

### `startSecondLife`
- Purpose: Initiates second life phase with new health/armor and slow death behavior
- Calls: `setMaxHealth`, `setArmorSetFlag`, `GameLogicRandomValue`

### `xfer`
- Purpose: Serializes module state for network synchronization
- Calls: `ActiveBody::xfer`

## Globals
- None

## Dependencies
- `ActiveBody.h` (base class)
- `SlowDeathBehavior.h` (interface)
- `Xfer.h` (serialization)
- `MultiIniFieldParse.h` (INI parsing)
