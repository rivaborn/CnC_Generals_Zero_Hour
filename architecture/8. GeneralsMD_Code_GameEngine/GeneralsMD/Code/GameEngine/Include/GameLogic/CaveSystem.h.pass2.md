# GeneralsMD/Code/GameEngine/Include/GameLogic/CaveSystem.h - Enhanced Analysis

## Architectural Role
This file defines the `CaveSystem` class, which manages the connectivity of cave systems on the map. It is part of the game logic subsystem and interacts with the tunnel tracking system to ensure proper pathfinding and connectivity for units moving through caves.

## Cross-References
### Incoming
- Likely called by map generation logic to initialize cave systems
- Used by unit movement AI to check cave connectivity
- Referenced by tunnel objects for connectivity validation

### Outgoing
- Uses `TunnelTracker` to manage individual tunnel connections
- Inherits from `SubsystemInterface` and `Snapshot` for engine integration

## Design Patterns
- **Singleton Pattern**: Global `TheCaveSystem` instance suggests singleton usage
- **Observer Pattern**: Implied by registration/unregistration of caves
- **Resource Pool**: Uses vector with potential nulls to manage tunnel trackers

Rules followed. Output under 400 tokens.
