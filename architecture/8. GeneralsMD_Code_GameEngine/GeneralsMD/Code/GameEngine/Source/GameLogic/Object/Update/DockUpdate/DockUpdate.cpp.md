# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/DockUpdate/DockUpdate.cpp

## Purpose
Manages docking behavior for objects in the game, handling approach positions, docking states, and position calculations.

## Responsibilities
- Manages approach positions for docking objects
- Handles docking state transitions (approach, enter, dock, exit)
- Computes docking positions using bone data or fallback logic
- Manages docking permissions and reservations
- Serializes docking state for network synchronization

## Key Types
- **DockUpdateModuleData (Class)**: Stores module configuration (approach positions, passthrough flag)
- **DockUpdate (Class)**: Core docking behavior manager
- **Coord3D (Struct)**: 3D coordinate representation

## Key Functions
### `reserveApproachPosition`
- Purpose: Reserves an approach position for a docking object
- Calls: `loadDockPositions`, `computeApproachPosition`

### `computeApproachPosition`
- Purpose: Calculates world-space approach position for a docker
- Calls: `loadDockPositions`, `ThePartitionManager->findPositionAround`

### `update`
- Purpose: Updates docking state and permissions
- Calls: `TheGameLogic->findObjectByID`

### `loadDockPositions`
- Purpose: Loads docking bone positions from the drawable
- Calls: `getDrawable()->getPristineBonePositions`

### `xfer`
- Purpose: Serializes docking state for network synchronization
- Calls: `UpdateModule::xfer`

## Globals
- **TheGameLogic (GameLogic**)**: Global game logic instance
- **ThePartitionManager (PartitionManager**)**: Global partition manager

## Dependencies
- `UpdateModule.h`, `Object.h`, `Drawable.h`, `PartitionManager.h`
- `GameLogic.h`, `Xfer.h`, `Debug.h`
- Uses `INI` parsing utilities
