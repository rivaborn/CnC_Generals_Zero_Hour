# GeneralsMD/Code/GameEngine/Include/GameLogic/ObjectTypes.h

## Purpose
Defines the `ObjectTypes` class for managing collections of object type names and providing utility methods for game logic.

## Responsibilities
- Maintain a list of object type names
- Provide methods to add/remove object types
- Check membership and iterate through the list
- Support snapshot serialization for save/load
- Interface with `Player` for object counting and build checks

## Key Types
- `ObjectTypes` (Class): Manages a collection of object type names with utility methods
- `Player` (Class): Reference to player object (external)
- `AsciiStringVec` (Type): Internal vector of object type names
- `AsciiStringVecIt` (Type): Iterator for the object type vector

## Key Functions
### `addObjectType`
- Purpose: Adds an object type to the internal list
- Calls: None

### `removeObjectType`
- Purpose: Removes an object type from the internal list
- Calls: None

### `isInSet`
- Purpose: Checks if an object type exists in the list
- Calls: None

### `prepForPlayerCounting`
- Purpose: Prepares data structures for counting objects by template for a player
- Calls: None

### `canBuildAny`
- Purpose: Checks if a player can build any of the object types in the list
- Calls: None

## Globals
- `ObjectTypes` (Class): Global instance of the ObjectTypes class

## Dependencies
- `Common/AsciiString.h`
- `Common/Snapshot.h`
- `MemoryPoolObject` (base class)
- `Snapshot` (base class)
- `Player` (external class)
- `ThingTemplate` (external class)
