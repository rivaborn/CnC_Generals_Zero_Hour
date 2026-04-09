# GeneralsMD/Code/Libraries/Source/WWVegas/WWSaveLoad/definitionfactorymgr.cpp

## Purpose
Manages a linked list of definition factories for the game's save/load system.

## Responsibilities
- Registers and unregisters definition factories
- Finds factories by class ID or name
- Iterates through factories by superclass
- Maintains the factory linked list

## Key Types
- `DefinitionFactoryMgrClass`: Manages the factory registry
- `DefinitionFactoryClass`: Base class for factories (external)

## Key Functions
### `Find_Factory(uint32 class_id)`
- Purpose: Finds a factory by its class ID
- Calls: None

### `Find_Factory(const char *name)`
- Purpose: Finds a factory by its name
- Calls: `stricmp`

### `Get_First(uint32 superclass_id)`
- Purpose: Gets the first factory of a given superclass
- Calls: `SuperClassID_From_ClassID`

### `Get_Next(DefinitionFactoryClass *curr_factory, uint32 superclass_id)`
- Purpose: Gets the next factory of a given superclass
- Calls: `SuperClassID_From_ClassID`

### `Register_Factory(DefinitionFactoryClass *factory)`
- Purpose: Registers a factory into the manager
- Calls: `Link_Factory`

### `Unregister_Factory(DefinitionFactoryClass *factory)`
- Purpose: Unregisters a factory from the manager
- Calls: `Unlink_Factory`

### `Link_Factory(DefinitionFactoryClass *factory)`
- Purpose: Links a factory into the list
- Calls: None

### `Unlink_Factory(DefinitionFactoryClass *factory)`
- Purpose: Removes a factory from the list
- Calls: None

## Globals
- `_FactoryListHead` (DefinitionFactoryClass*): Head of the factory linked list

## Dependencies
- `definitionfactory.h` (DefinitionFactoryClass)
- `wwdebug.h` (WWASSERT)
- `string.h` (stricmp)
- `SuperClassID_From_ClassID` (external function)
