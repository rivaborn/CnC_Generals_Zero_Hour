# Generals/Code/GameEngine/Source/Common/Thing/ModuleFactory.cpp

## Purpose
The `ModuleFactory` class is responsible for creating and managing module templates and instances used in the game engine. It acts as a singleton to ensure centralized control over module creation.

## Responsibilities
- Manages module templates and their instantiation.
- Provides methods to find, create, and initialize modules based on configuration data.
- Handles the lifecycle of module data, including initialization and cleanup.

## Key Types
- `ModuleFactory` (Class): Manages module templates and instances.
- `ModuleTemplate` (Struct): Stores information about a module template, including creation procedures and interface masks.
- `ModuleData` (Class): Represents configuration data for a module.

## Key Functions
### ModuleFactory::init
- Purpose: Initializes the module factory by adding various module types to its internal map.
- Calls:
  - `addModule`

### ModuleFactory::findModuleInterfaceMask
- Purpose: Retrieves the interface mask for a given module name and type.
- Calls:
  - `findModuleTemplate`

### ModuleFactory::newModuleDataFromINI
- Purpose: Creates a new `ModuleData` instance from an INI file, setting up the module with configuration data.
- Calls:
  - `findModuleTemplate`
  - `(*moduleTemplate->m_createDataProc)`

### ModuleFactory::newModule
- Purpose: Instantiates a new module based on its name and type, using the appropriate template.
- Calls:
  - `findModuleTemplate`
  - `(*mt->m_createProc)`

## Globals
- `TheModuleFactory` (ModuleFactory*): The singleton instance of the module factory.

## Dependencies
- Key includes:
  - "Common/Module.h"
  - "Common/ModuleFactory.h"
  - "GameLogic/Module/*" (various behavior, die, update, upgrade, create, damage, collide, body, and special power modules)
  - "GameClient/Module/*" (client-specific update modules)
