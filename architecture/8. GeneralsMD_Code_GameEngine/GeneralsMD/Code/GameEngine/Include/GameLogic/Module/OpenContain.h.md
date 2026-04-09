# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/OpenContain.h

## Purpose
Defines the OpenContain module, which handles containment of objects within other objects (e.g., vehicles carrying units).

## Responsibilities
- Manages object containment, entry/exit logic, and passenger behavior
- Handles collisions, damage, and death events for containers
- Controls fire points, rally points, and passenger permissions
- Manages sounds and visual effects for loading/unloading

## Key Types
- **OpenContainModuleData (Class)**: Module data containing containment settings (capacity, sounds, permissions)
- **OpenContain (Class)**: Core containment module implementing multiple interfaces (Update, Contain, Collide, Die, Damage, Exit)
- **ObjectEnterExitMap (Class)**: Maps ObjectID to entry/exit states
- **OpenContainMagicEnum (Enum)**: Placeholder enum (not inferable)
- **OpenContain_GLUE_NOT_IMPLEMENTED (Enum)**: Placeholder enum (not inferable)
- **MAX_FIRE_POINTS (Enum)**: Constant for max fire points (32)

## Key Functions
### `update()`
- Purpose: Called once per frame to update containment logic.
- Calls: `monitorConditionChanges`, `redeployOccupants`, `pruneDeadWanters`

### `onCollide(Object*, const Coord3D*, const Coord3D*)`
- Purpose: Handles collision events for the container.
- Calls: None visible in header.

### `addToContain(Object*)`
- Purpose: Adds an object to the containment list.
- Calls: `addToContainList`, `addOrRemoveObjFromWorld`

### `removeFromContain(Object*, Bool)`
- Purpose: Removes an object from the containment list.
- Calls: `removeFromContainViaIterator`, `addOrRemoveObjFromWorld`

### `orderAllPassengersToExit(CommandSourceType, Bool)`
- Purpose: Orders all passengers to exit the container.
- Calls: None visible in header.

### `isValidContainerFor(const Object*, Bool)`
- Purpose: Checks if an object can be contained.
- Calls: None visible in header.

## Globals
- **m_containList (ContainedItemsList)**: List of contained objects
- **m_containListSize (UnsignedInt)**: Size of the containment list
- **m_stealthUnitsContained (UnsignedInt)**: Count of stealth units inside
- **m_firePoints (Matrix3D[MAX_FIRE_POINTS])**: Positions for passenger fire points
- **m_rallyPoint (Coord3D)**: Rally point for exiting units
- **m_loadSoundsEnabled (Bool)**: Flag to enable/disable load sounds

## Dependencies
- **BehaviorModule.h**, **
