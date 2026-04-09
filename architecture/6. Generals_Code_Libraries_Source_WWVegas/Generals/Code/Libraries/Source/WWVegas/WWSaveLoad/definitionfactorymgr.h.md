# Generals/Code/Libraries/Source/WWVegas/WWSaveLoad/definitionfactorymgr.h

## Purpose
Manages registration and lookup of definition factories used in the game's save/load system.

## Responsibilities
- Registers and unregisters definition factories
- Finds factories by class ID or name
- Enumerates factories by superclass or all factories
- Maintains a linked list of registered factories

## Key Types
- DefinitionFactoryClass (Class): Base class for definition factories (not defined here)
- DefinitionFactoryMgrClass (Class): Singleton manager for definition factories

## Key Functions
### Find_Factory (uint32 class_id)
- Purpose: Finds a factory by its class ID
- Calls: Not inferable

### Find_Factory (const char *name)
- Purpose: Finds a factory by its name
- Calls: Not inferable

### Register_Factory
- Purpose: Registers a new factory with the manager
- Calls: Link_Factory

### Unregister_Factory
- Purpose: Unregisters a factory from the manager
- Calls: Unlink_Factory

### Get_First (uint32 superclass_id)
- Purpose: Gets the first factory of a given superclass
- Calls: Not inferable

### Get_Next (DefinitionFactoryClass *current, uint32 superclass_id)
- Purpose: Gets the next factory of a given superclass
- Calls: Not inferable

### Get_First (void)
- Purpose: Gets the first registered factory
- Calls: Not inferable

### Get_Next (DefinitionFactoryClass *current)
- Purpose: Gets the next registered factory
- Calls: Not inferable

### Link_Factory
- Purpose: Links a factory into the internal list
- Calls: Not inferable

### Unlink_Factory
- Purpose
