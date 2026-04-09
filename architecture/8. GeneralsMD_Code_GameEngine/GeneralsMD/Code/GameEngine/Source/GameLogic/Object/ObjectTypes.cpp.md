# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/ObjectTypes.cpp

## Purpose
Manages collections of object types (e.g., units, buildings) and their associated operations like addition, removal, and querying.

## Responsibilities
- Maintains a list of object type names
- Provides methods to check if an object type is in the list
- Supports serialization/deserialization for save/load
- Interfaces with the ThingFactory to resolve object templates
- Checks build permissions for a given player

## Key Types
- `ObjectTypes` (Class): Manages a set of object type names and related operations
- `AsciiStringVec` (Type): Underlying container for storing object type names

## Key Functions
### `addObjectType`
- Purpose: Adds an object type to the internal list if not already present
- Calls: `isInSet`

### `removeObjectType`
- Purpose: Removes an object type from the internal list
- Calls: `isInSet`, `std::find`

### `isInSet`
- Purpose: Checks if an object type (by name or template) exists in the list
- Calls: `std::find`, `ThingTemplate::getName`

### `prepForPlayerCounting`
- Purpose: Prepares a list of ThingTemplates and counts for player-specific logic
- Calls: `TheThingFactory->findTemplate`

### `canBuildAny`
- Purpose: Checks if a player can build any object in this list
- Calls: `TheThingFactory->findTemplate`, `Player::canBuild`

### `xfer`
- Purpose: Serializes/deserializes the ObjectTypes data
- Calls: `Xfer::xferVersion`, `Xfer::xferAsciiString`, `Xfer::xferUnsignedShort`

## Globals
- `TheThingFactory` (ThingFactory*): Global factory for resolving object templates

## Dependencies
- `PreRTS.h`, `GameLogic/ObjectTypes.h`
- `Common/GameState.h`, `Common/Player.h`, `Common/ThingFactory.h`, `Common/ThingTemplate.h`, `Common/Xfer.h`
- `AsciiString`, `std::vector`, `std::find`, `Xfer`, `ThingTemplate`, `Player`
