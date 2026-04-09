# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/UndeadBody.h

## Purpose
Defines the UndeadBody module, which handles objects that respawn with reduced health after first death.

## Responsibilities
- Manages first-death interception and health reset
- Controls second-life behavior for "undead" objects
- Extends ActiveBody functionality with resurrection logic

## Key Types
- **UndeadBodyModuleData (Class)**: Stores module configuration (second-life max health)
- **UndeadBody (Class)**: Implements undead resurrection behavior
- **UndeadBodyMagicEnum (Enum)**: Not inferable (likely unused placeholder)
- **Object (Class)**: Forward reference to base game object

## Key Functions
### UndeadBody::attemptDamage
- Purpose: Handles damage with special first-death interception logic
- Calls: startSecondLife

### UndeadBody::startSecondLife
- Purpose: Resets health values and enables normal death handling
- Calls: Not inferable

### UndeadBodyModuleData::buildFieldParse
- Purpose: Parses module data from configuration files
- Calls: Not inferable

## Globals
- None

## Dependencies
- ActiveBody.h (base class)
- MultiIniFieldParse (for config parsing)
- Thing (forward reference)
- DamageInfo (damage handling struct)
