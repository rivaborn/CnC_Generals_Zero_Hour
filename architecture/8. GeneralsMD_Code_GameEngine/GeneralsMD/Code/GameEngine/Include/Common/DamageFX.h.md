# GeneralsMD/Code/GameEngine/Include/Common/DamageFX.h

## Purpose
Defines the DamageFX system for handling audio-video effects when objects take damage in the game.

## Responsibilities
- Manages damage effect descriptions (minor/major effects per damage type)
- Provides a store for DamageFX objects accessible by game objects
- Handles parsing of damage effect definitions from INI files
- Throttles damage effects to prevent visual/audio spam

## Key Types
- **DamageFX (Class)**: Describes how an object reacts to damage with A/V effects.
- **DFX (Struct)**: Internal structure holding damage thresholds and effect lists.
- **DamageFXStore (Class)**: Singleton store managing all DamageFX objects.
- **DamageFXMap (Class)**: Internal hash map for storing DamageFX objects.

## Key Functions
### DamageFX::doDamageFX
- Purpose: Executes the appropriate A/V effect for a given damage type and amount.
- Calls: getDamageFXList

### DamageFXStore::findDamageFX
- Purpose: Retrieves a DamageFX by name from the store.
- Calls: None

### DamageFXStore::parseDamageFXDefinition
- Purpose: Parses damage effect definitions from INI files.
- Calls: None

## Globals
- **TheDamageFXStore (DamageFXStore*)**: Global instance of the DamageFX store.

## Dependencies
- "Common/GameCommon.h", "Common/NameKeyGenerator.h", "Common/STLTypedefs.h", "GameLogic/Damage.h"
- INI class, FXList class, Object class, FieldParse class
