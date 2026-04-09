# GeneralsMD/Code/GameEngine/Source/GameLogic/AI/AIPathfind.cpp

## Purpose
Implements the AI pathfinding system for the game, handling movement calculations, obstacle avoidance, and path optimization.

## Responsibilities
- Manages pathfinding for ground and air units
- Handles obstacle detection and avoidance
- Optimizes paths for performance
- Supports attack pathfinding with line-of-sight checks
- Manages pathfinding zones and layers

## Key Types
- **PathNode (Class)**: Represents a node in a path with position and optimization data
- **Path (Class)**: Manages a sequence of path nodes and optimization state
- **Pathfinder (Class)**: Main pathfinding system with search algorithms
- **TCheckMovementInfo (Struct)**: Contains movement validation parameters
- **PathfindCell (Class)**: Grid cell used in pathfinding with state tracking

## Key Functions
### findAttackPath
- Purpose: Finds a path to attack a target while maintaining line of sight
- Calls: checkDestination, isAttackViewBlockedByObstacle, examineNeighboringCells

### findSafePath
- Purpose: Finds a path avoiding repulsor zones
- Calls: checkDestination, examineNeighboringCells

### buildActualPath
- Purpose: Constructs a Path object from pathfinding results
- Calls: PathNode operations, optimization routines

### examineNeighboringCells
- Purpose: Evaluates adjacent cells for pathfinding
- Calls: checkForMovement, getCell, various movement validation functions

## Globals
- **frameToShowObstacles (Int)**: Debug flag for visualizing obstacles
- **ZONE_UPDATE_FREQUENCY (UnsignedInt)**: How often to update pathfinding zones
- **COST_ORTHOGONAL/COST_DIAGONAL (Int)**: Movement cost constants
- **COST_TO_DISTANCE_FACTOR (Real)**: Converts path cost to distance

## Dependencies
- GameLogic headers: AIPathfind.h, AI.h, GameLogic.h
- Common headers: PerfTimer.h, Player.h, GlobalData.h
- GameClient headers: Line2D.h
- Module headers: ContainModule.h, AIUpdate.h, PhysicsUpdate.h
- Other: ThingTemplate.h, ThingFactory.h, PartitionManager.h, TerrainLogic.h, Weapon.h
