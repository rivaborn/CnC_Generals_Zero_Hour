# GeneralsMD/Code/GameEngine/Include/Common/TunnelTracker.h

## Purpose
Manages communal passenger lists for tunnels in a player's brain, similar to ContainModule but for players without modules.

## Responsibilities
- Track objects contained within tunnels
- Manage tunnel creation/destruction events
- Handle healing of contained objects
- Maintain nemesis targeting for tunnel defense

## Key Types
- **TunnelTracker (Class)**: Manages tunnel contents and state
- **TunnelTrackerMagicEnum (Enum)**: Not inferable
- **TunnelTracker_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### iterateContained
- Purpose: Apply a function to all contained objects
- Calls: None visible

### addToContainList
- Purpose: Add an object to the tunnel's contain list
- Calls: None visible

### removeFromContain
- Purpose: Remove an object from the tunnel's contain list
- Calls: None visible

### onTunnelCreated
- Purpose: Handle tunnel creation events
- Calls: None visible

### onTunnelDestroyed
- Purpose: Handle tunnel destruction events
- Calls: None visible

### healObjects
- Purpose: Heal all objects within the tunnel
- Calls: None visible

### updateNemesis
- Purpose: Update the current nemesis target
- Calls: None visible

## Globals
- None

## Dependencies
- Common/GameType.h
- Common/GameMemory.h
- Common/Snapshot.h
- GameLogic/Module/ContainModule.h
- std::list
- MemoryPoolObject
- Snapshot
- ContainIterateFunc
- Object
- ObjectID
- Xfer
