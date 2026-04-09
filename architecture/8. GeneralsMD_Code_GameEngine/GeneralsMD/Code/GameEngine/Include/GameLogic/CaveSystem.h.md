# GeneralsMD/Code/GameEngine/Include/GameLogic/CaveSystem.h

## Purpose
Manages cave systems and tunnel connectivity on the map, tracking which caves are connected and handling registration/unregistration.

## Responsibilities
- Tracks connectedness of cave systems
- Manages tunnel trackers for each cave
- Handles registration/unregistration of caves
- Provides connectivity checks between caves

## Key Types
- **CaveSystem (Class)**: Main system for managing cave connectivity and tunnel trackers
- **TunnelTracker (Class)**: Tracks tunnels for a specific cave (external)
- **Object (Class)**: Base game object (external)

## Key Functions
### `CaveSystem::canSwitchIndexToIndex`
- Purpose: Checks if switching between two cave indices is allowed
- Calls: None

### `CaveSystem::registerNewCave`
- Purpose: Registers a new cave with a given index
- Calls: None

### `CaveSystem::unregisterCave`
- Purpose: Removes a cave from the system
- Calls: None

### `CaveSystem::getTunnelTrackerForCaveIndex`
- Purpose: Retrieves the tunnel tracker for a specific cave index
- Calls: None

### `CaveSystem::xfer`
- Purpose: Handles snapshot serialization
- Calls: None

## Globals
- **TheCaveSystem (CaveSystem*)**: Global instance of the cave system

## Dependencies
- `Common/Snapshot.h` (Snapshot)
- `Common/SubsystemInterface.h` (SubsystemInterface)
- `std::vector` (for tunnel tracker storage)
