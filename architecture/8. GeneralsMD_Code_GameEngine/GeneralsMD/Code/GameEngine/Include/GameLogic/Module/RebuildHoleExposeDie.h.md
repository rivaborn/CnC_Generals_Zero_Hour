# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/RebuildHoleExposeDie.h

## Purpose
Defines a module that creates a rebuild hole when a structure dies, allowing automatic reconstruction.

## Responsibilities
- Creates a rebuild hole object upon structure death
- Transfers attackers to the new hole if configured
- Manages hole health and naming via module data
- Handles death event logic for structures

## Key Types
- **Thing (Class)**: Base class for game objects (forward reference)
- **RebuildHoleExposeDieModuleData (Class)**: Stores hole configuration (name, health, attacker transfer flag)
- **RebuildHoleExposeDie (Class)**: Module implementing the rebuild hole creation logic
- **RebuildHoleExposeDieMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **RebuildHoleExposeDie_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum)

## Key Functions
### RebuildHoleExposeDieModuleData::buildFieldParse
- Purpose: Parses INI configuration for module data
- Calls: Not inferable (MultiIniFieldParse methods)

### RebuildHoleExposeDie::onDie
- Purpose: Handles structure death to create rebuild hole
- Calls: Not inferable (DieModule base class methods)

## Globals
None

## Dependencies
- `Common/INI.h` (INI parsing)
- `GameLogic/Module/DieModule.h` (base module class)
- `MultiIniFieldParse` (INI parsing utility)
- `AsciiString`, `Real`, `Bool` (primitive types)
- `DamageInfo` (damage event data, forward reference)
