# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/SpecialPower/OCLSpecialPower.cpp - Enhanced Analysis

## Architectural Role
This file implements the core logic for special powers that spawn objects via ObjectCreationLists (OCLs), bridging the game's power system with its object instantiation framework. It handles location-based power execution, upgrade-dependent OCL selection, and terrain-aware positioning.

## Cross-References
### Incoming
- **UI/Command System**: Calls `doSpecialPowerAtLocation`, `doSpecialPowerAtObject`, and `doSpecialPower` when players activate special abilities.
- **Networking**: Likely invoked during power execution serialization via `xfer`/`crc` methods.
- **AI System**: May use `doSpecialPowerAtLocation` for scripted power activations.

### Outgoing
- **ObjectCreationList**: Delegates object spawning via `ObjectCreationList::create`.
- **TerrainLogic**: Uses `findClosestEdgePoint`/`findFarthestEdgePoint` for edge-based creation.
- **PartitionManager**: Adjusts positions for passability via `findPositionAround`.
- **ThingFactory**: Resolves reference objects via `getReferenceThingTemplate`.

## Design Patterns
- **Strategy Pattern**: Encapsulates different creation location strategies (edge/above/target) in a switch-case.
- **Template Method**: Extends `SpecialPowerModule` with `doSpecialPowerAtLocation` while preserving base behavior.
- **Dependency Injection**: Receives `ObjectCreationList` via `findOCL`, allowing runtime selection based on upgrades.
