# GeneralsMD/Code/GameEngine/Include/GameLogic/AIPathfind.h

## Purpose
Header file defining the AI pathfinding system for Command & Conquer Generals Zero Hour.

## Responsibilities
- Declares pathfinding data structures (PathNode, Path, PathfindCell)
- Defines the Pathfinder class and its interfaces
- Provides pathfinding utilities and grid management
- Handles obstacle classification and movement validation

## Key Types
- **PathNode (Class)**: Represents nodes in a path
- **Path (Class)**: Encapsulates a complete path between points
- **PathfindCell (Class)**: Represents one cell in the pathfinding grid
- **Pathfinder (Class)**: Main pathfinding engine
- **PathfindLayer (Class)**: Manages pathfinding for bridges/walls
- **PathfindZoneManager (Class)**: Handles pathfinding zones
- **CellType (Enum)**: Cell terrain classification
- **CellFlags (Enum)**: Unit presence flags

## Key Functions
### Pathfinder::findPath
- Purpose: Find a valid path between two locations
- Calls: internalFindPath, findHierarchicalPath

### Pathfinder::validMovementPosition
- Purpose: Check if a position is valid for movement
- Calls: getCell, locomotorSet.getValidSurfaces()

### Pathfinder::classifyMapCell
- Purpose: Classify a map cell's terrain type
- Calls: None visible

### Pathfinder::worldToCell
- Purpose: Convert world coordinates to grid cell
- Calls: None

## Globals
- **PATHFIND_CLOSE_ENOUGH (Real)**: Movement tolerance threshold
- **PATH_MAX_PRIORITY (Int)**: Maximum path priority value
- **PATHFIND_CELL_SIZE (Real)**: Size of pathfinding cells

## Dependencies
- Common/GameType.h
- Common/GameMemory.h
- Common/Snapshot.h
- GameLogic/LocomotorSet.h
- GameLogic/GameLogic.h
- Forward declarations: Bridge, Object, Weapon classes
