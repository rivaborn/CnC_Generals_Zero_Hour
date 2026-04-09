# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Contain/OpenContain.cpp

## Purpose
Implements the OpenContain module for object containment in the SAGE engine, handling loading/unloading, damage propagation, and container logic.

## Responsibilities
- Manages object containment (loading/unloading passengers)
- Handles container-specific logic (doors, rally points, fire permissions)
- Propagates damage to contained units
- Manages container state serialization/deserialization
- Validates containment rules (player alliances, kind restrictions)

## Key Types
- **OpenContainModuleData (Class)**: Container configuration (max capacity, allowed kinds, sounds)
- **DropData (Class)**: Data for unloading objects (position, direction)
- **ObjectEnterExitType (Enum)**: Tracks enter/exit requests (want to enter/exit)

## Key Functions
### `addToContain(Object *rider)`
- Purpose: Adds an object to the container and triggers containment events
- Calls: `checkAndDetonateBoobyTrap`, `addToContainList`, `onContaining`, `onContainedBy`, `doLoadSound`

### `removeFromContain(Object *rider, Bool exposeStealthUnits)`
- Purpose: Removes an object from the container and triggers removal events
- Calls: `removeFromContainList`, `onRemoving`, `onRemovedFrom`, `doUnloadSound`

### `processDamageToContained(Real percentDamage)`
- Purpose: Applies damage to all contained units
- Calls: `attemptDamage` on each contained object

### `testForAttackingProc(Object *obj, void *userData)`
- Purpose: Checks if an object is attacking (callback for iteration)
- Calls: `testStatus` on the object

## Globals
- **ThePartitionManager**: Manages spatial partitioning of game objects
- **TheAI**: Provides pathfinding services
- **TheGameLogic**: Core game logic system

## Dependencies
- **Common**: BitFlagsIO, GameAudio, GameState, Module, Player, RandomValue, ThingTemplate, Xfer
- **GameClient**: Drawable, InGameUI, ControlBar
- **GameLogic**: AIPathfind, GameLogic, Module headers (OpenContain, AIUpdate, PhysicsUpdate, StealthUpdate, BodyModule), Object, PartitionManager, Weapon
