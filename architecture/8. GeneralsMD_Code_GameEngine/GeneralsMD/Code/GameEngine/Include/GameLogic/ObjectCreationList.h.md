# GeneralsMD/Code/GameEngine/Include/GameLogic/ObjectCreationList.h

## Purpose
Defines the object creation system for game entities, including nuggets, lists, and the store that manages them.

## Responsibilities
- Declares `ObjectCreationNugget` (abstract base class for object creation logic)
- Defines `ObjectCreationList` (container for nuggets that creates objects in sequence)
- Implements `ObjectCreationListStore` (global registry for all creation lists)
- Provides static creation methods for convenience
- Manages memory via `MemoryPoolObject`

## Key Types
- `ObjectCreationNugget` (Class): Abstract base class for object creation logic
- `ObjectCreationList` (Class): Container for nuggets that creates objects sequentially
- `ObjectCreationListStore` (Class): Global registry for all creation lists
- `ObjectCreationNuggetVector` (Class): Typedef for `std::vector<ObjectCreationNugget*>`
- `ObjectCreationListMap` (Class): Typedef for `std::map<NameKeyType, ObjectCreationList>`

## Key Functions
### `ObjectCreationNugget::create`
- Purpose: Abstract method to create an object
- Calls: None (pure virtual)

### `ObjectCreationList::createInternal`
- Purpose: Internal method to create objects from the list
- Calls: `ObjectCreationNugget::create` for each nugget

### `ObjectCreationListStore::findObjectCreationList`
- Purpose: Retrieves a creation list by name
- Calls: None

### `ObjectCreationListStore::parseObjectCreationListDefinition`
- Purpose: Parses INI definitions for creation lists
- Calls: None

## Globals
- `TheObjectCreationListStore` (ObjectCreationListStore*): Global instance of the store

## Dependencies
- `Common/GameMemory.h` (MemoryPoolObject)
- `INI` (Class)
- `Object` (Class)
- `Coord3D` (Struct)
- `std::vector`, `std::map`, `std::less` (STL)
