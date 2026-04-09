# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/ProneUpdate.h

## Purpose
Defines the prone behavior module for game entities, handling cowering animations and effects when damaged.

## Responsibilities
- Manages prone state transitions for game objects
- Calculates prone duration based on damage received
- Controls prone visual/audio effects
- Provides module data for configuration

## Key Types
- **ProneUpdateModuleData (Class)**: Stores module configuration (damage-to-frames ratio)
- **ProneUpdate (Class)**: Implements prone behavior logic
- **ProneUpdateMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **Thing (Class)**: Forward reference to game object
- **DamageInfo (Class)**: Forward reference to damage data

## Key Functions
### ProneUpdate::goProne
- Purpose: Initiates prone state based on damage info
- Calls: Not inferable

### ProneUpdate::update
- Purpose: Updates prone state each frame
- Calls: Not inferable

### ProneUpdate::startProneEffects
- Purpose: Activates prone visual/audio effects
- Calls: Not inferable

### ProneUpdate::stopProneEffects
- Purpose: Deactivates prone visual/audio effects
- Calls: Not inferable

## Globals
- None

## Dependencies
- UpdateModule.h (base class)
- MultiIniFieldParse (for configuration parsing)
- Memory pool macros (MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE)
- Module system macros (MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA)
