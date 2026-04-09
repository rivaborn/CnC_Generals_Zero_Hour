# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/PartitionManager.cpp

## Purpose
Manages spatial partitioning of game objects for efficient spatial queries, collision detection, and threat/value calculations.

## Responsibilities
- Spatial partitioning of game objects into cells
- Collision detection between objects
- Threat and value calculations for AI targeting
- Line-of-sight and shroud management
- Object filtering and iteration

## Key Types
- **ThreatValueParms (struct)**: Parameters for threat/value calculations
- **CollideInfo (class)**: Collision information for objects
- **CellValueProcParms (struct)**: Parameters for cell value queries
- **CollideTestProc (typedef)**: Function pointer for collision tests
- **DistCalcProc (typedef)**: Function pointer for distance calculations
- **PartitionContactListNode (class)**: Node for contact lists
- **PartitionContactList (class)**: Contact list for collision handling
- **TerrainExtremeData (class)**: Terrain height data

## Key Functions
### filtersAllow
- Purpose: Check if object passes all partition filters
- Calls: PartitionFilter::allow

### cellValueProc
- Purpose: Calculate value/threat for a partition cell
- Calls: PartitionCell::getCashValue, PartitionCell::getThreatValue

### hLineAddLooker/hLineRemoveLooker
- Purpose: Add/remove line-of-sight for a player across cells
- Calls: PartitionCell::addLooker, PartitionCell::removeLooker

### hLineAddThreat/hLineRemoveThreat
- Purpose: Add/remove threat values across cells
- Calls: PartitionCell::addThreatValue, PartitionCell::removeThreatValue

### collision detection functions (xy_collideTest_*, collideTest_*)
- Purpose: Various collision detection implementations
- Calls: None (pure geometry calculations)

### distance calculation functions (distCalcProc_*)
- Purpose: Calculate distances between objects
- Calls: None (pure geometry calculations)

## Globals
- **HUGE_DIST_SQR (Real)**: Large distance value for comparisons
- **TheContactList (PartitionContactList*)**: Global contact list instance
- **theDistCalcProcs (DistCalcProc*)**: Array of distance calculation functions
- **theCollideTestProcs (CollideTestProc*)**: Array of collision test functions
- **ThePartitionManager (PartitionManager*)**: Global partition manager instance
- **ringSpacing (Real)**: Spacing for circular partitions

## Dependencies
- Common game engine headers (ActionManager, GameEngine, etc.)
- GameLogic headers (Object, PartitionManager, etc.)
- Geometry and collision detection utilities
- Memory management and debugging utilities
