# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Contain/GarrisonContain.cpp - Enhanced Analysis

## Architectural Role
This file implements the garrison containment system, bridging between the physical structure (via `BodyModule`) and contained units (via `OpenContain`). It handles spatial placement of garrisoned units, firing position logic, and damage state transitions - critical for multi-unit tactics in the game.

## Cross-References
### Incoming
- `BodyModule` calls `onBodyDamageStateChange` to handle structure damage events
- `AIUpdate` likely invokes garrison point management functions during unit movement
- `Weapon` systems call `attemptBestFirePointPosition` for range checking

### Outgoing
- Calls `ThingFactory` for creating drawable effects
- Uses `PartitionManager` for spatial queries during garrison point placement
- Interacts with `GameClient` for drawable effect management

## Design Patterns
- **Strategy Pattern**: Different garrison behaviors (mobile vs stationary) are configured via `GarrisonContainModuleData`
- **Composite Pattern**: Manages collection of garrison points and their occupants as a unified system
- **Observer Pattern**: Reacts to damage state changes via `onBodyDamageStateChange` callback

*Not inferable*: Exact implementation of station point loading from skeletal bones.
