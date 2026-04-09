# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/RadarUpdate.h - Enhanced Analysis

## Architectural Role
This file defines the radar functionality module within the game's object component system. It extends the `UpdateModule` base class to provide periodic radar state updates and configuration parsing for radar towers and similar objects.

## Cross-References
### Incoming
- Likely called by `Thing` objects (e.g., radar towers) during their update cycle
- Referenced in module factory/registration code (via `MAKE_STANDARD_MODULE_MACRO`)

### Outgoing
- Calls `UpdateModuleData::buildFieldParse` for base INI parsing
- Uses `MultiIniFieldParse` for configuration parsing
- Depends on `INI` namespace for parsing utilities

## Design Patterns
- **Component Pattern**: Implements radar as a modular component attachable to game objects
- **Data-Driven Design**: Uses `buildFieldParse` to configure behavior via INI files
- **State Machine**: Manages radar activation/extension states (`m_radarActive`, `m_extendComplete`)
