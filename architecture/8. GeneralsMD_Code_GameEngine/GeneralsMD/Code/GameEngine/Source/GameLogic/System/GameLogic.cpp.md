# GeneralsMD/Code/GameEngine/Source/GameLogic/System/GameLogic.cpp

## Purpose
Core game logic implementation for Command & Conquer Generals/Zero Hour, handling game state, object management, and game flow.

## Responsibilities
- Manages game objects and their lifecycle
- Handles game state transitions and loading/saving
- Implements game progression and victory conditions
- Manages player sides, colors, and starting positions
- Controls game timing and frame updates

## Key Types
- `GameLogic` (Class): Main game logic controller
- `LOAD_PROGRESS_*` (Enums): Loading screen progress states
- `OBJ_HASH_SIZE` (Enum): Object hash table size

## Key Functions
### `findNamedWaypoint`
- Purpose: Locates a waypoint by name
- Calls: `TheTerrainLogic->getFirstWaypoint()`, `way->getNext()`

### `setFPMode`
- Purpose: Configures floating-point precision and rounding
- Calls: `_fpreset()`, `_statusfp()`, `_controlfp()`

### `placeObjectAtPosition`
- Purpose: Places an object at a specific position
- Calls: `TheThingFactory->newObject()`, `obj->setPosition()`

### `placeNetworkBuildingsForPlayer`
- Purpose: Places initial buildings for a player
- Calls: `TheThingFactory->newObject()`, `obj->setPosition()`

### `populateRandomSideAndColor`
- Purpose: Assigns random sides and colors to players
- Calls: `TheSidesList->getSide()`, `ThePlayerList->getPlayer()`

### `populateRandomStartPosition`
- Purpose: Assigns random starting positions to players
- Calls: `TheTerrainLogic->getStartPosition()`, `ThePlayerList->getPlayer()`

## Globals
- `TheGameLogic` (GameLogic*): Singleton instance of GameLogic
- `inCRCGen` (Bool): CRC generation flag

## Dependencies
- GameEngine headers (Common/, GameClient/, GameLogic/, GameNetwork/)
- W3D rendering system
- Scripting and AI systems
- Networking and multiplayer components
