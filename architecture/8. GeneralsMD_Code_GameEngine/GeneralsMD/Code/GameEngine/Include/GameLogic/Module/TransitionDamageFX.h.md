# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/TransitionDamageFX.h

## Purpose
Defines a damage module that triggers visual effects when a unit transitions between damage states.

## Responsibilities
- Parses INI configuration for damage effects
- Manages FX lists, object creation lists, and particle systems
- Handles damage state transitions (damaged, really damaged, rubble)
- Tracks active particle systems for cleanup

## Key Types
- **TransitionDamageFXModuleData (Class)**: Holds configuration for damage effects
- **TransitionDamageFX (Class)**: Implements the damage module behavior
- **FXLocInfo (Struct)**: Stores location data for effects (bone/coord)
- **FXDamageFXListInfo (Struct)**: Associates FXList with location info
- **FXDamageOCLInfo (Struct)**: Associates ObjectCreationList with location info
- **FXDamageParticleSystemInfo (Struct)**: Associates ParticleSystemTemplate with location info

## Key Functions
### TransitionDamageFXModuleData::buildFieldParse
- Purpose: Registers INI field parsers for module data
- Calls: DamageModuleData::buildFieldParse

### TransitionDamageFXModuleData::parseFXList
- Purpose: Parses FXList references from INI
- Calls: Not inferable

### TransitionDamageFXModuleData::parseObjectCreationList
- Purpose: Parses ObjectCreationList references from INI
- Calls: Not inferable

### TransitionDamageFXModuleData::parseParticleSystem
- Purpose: Parses ParticleSystemTemplate references from INI
- Calls: Not inferable

### TransitionDamageFX::onBodyDamageStateChange
- Purpose: Handles damage state transitions and triggers effects
- Calls: Not inferable

## Globals
- **DAMAGE_MODULE_MAX_FX (Enum)**: Maximum number of effects per damage state (12)

## Dependencies
- "GameClient/ParticleSys.h"
- "GameLogic/Module/DamageModule.h"
- "GameLogic/Module/BodyModule.h"
- INI parsing utilities
- Memory pool macros (MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA, MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE)
