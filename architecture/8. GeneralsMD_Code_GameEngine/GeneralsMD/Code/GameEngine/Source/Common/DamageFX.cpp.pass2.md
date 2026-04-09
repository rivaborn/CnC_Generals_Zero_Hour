# GeneralsMD/Code/GameEngine/Source/Common/DamageFX.cpp - Enhanced Analysis

## Architectural Role
This file implements the damage effect system, bridging the damage calculation logic (`Damage.h`) with the visual/audio FX system (`FXList.h`). It acts as a configuration layer that maps damage types/amounts to specific effects, with veterancy-aware scaling.

## Cross-References
### Incoming
- `INIDamageFX.cpp` calls `parseDamageFXDefinition` to initialize damage FX from INI files
- `TransitionDamageFX.cpp` uses `doDamageFX` to apply effects during damage transitions

### Outgoing
- Calls `FXList::doFXObj` to execute visual/audio effects
- Uses `INI` parsing utilities for configuration loading
- Depends on `Object` for veterancy level queries

## Design Patterns
- **Strategy Pattern**: Damage FX selection (`getDamageFXList`) chooses between major/minor effects based on damage amount
- **Template Method**: Parser methods (`parseAmount`, `parseMajorFXList`) use `parseCommonStuff` as a shared setup step
- **Singleton**: `TheDamageFXStore` provides global access to damage FX definitions (implicit via global pointer)

*Not inferable*: No clear use of Observer or Factory patterns in this file.
