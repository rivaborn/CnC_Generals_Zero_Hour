# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/StructureCollapseUpdate.cpp - Enhanced Analysis

## Architectural Role
This file implements the collapse animation system for structures, bridging game logic and visual effects. It manages timed destruction sequences, coordinates with the FX and OCL systems, and handles physics-based collapse behavior.

## Cross-References
### Incoming
- **Damage system**: Calls `beginStructureCollapse` when structures are destroyed
- **Update loop**: Invokes `update` each frame via the module system
- **INI parser**: Uses `parseFX`/`parseOCL` during module data initialization

### Outgoing
- **FXList system**: Triggers effects via `FXList::doFXPos`
- **ObjectCreationList**: Spawns debris/objects via `ObjectCreationList::create`
- **BoneFXUpdate**: Communicates with skeletal animation system in `doCollapseDoneStuff`
- **GameLogic**: Uses `TheGameLogic->getFrame()` for timing

## Design Patterns
- **Strategy Pattern**: Phase-based behavior (INITIAL/DELAY/BURST/FINAL) encapsulated in `doPhaseStuff`
- **Observer Pattern**: Reacts to damage events via `beginStructureCollapse`
- **Template Method**: `UpdateModule` base class defines update/xfer interfaces

*Not inferable*: Exact synchronization mechanism with networking layer.
