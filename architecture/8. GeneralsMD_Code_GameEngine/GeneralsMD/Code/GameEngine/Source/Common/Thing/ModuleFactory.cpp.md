# GeneralsMD/Code/GameEngine/Source/Common/Thing/ModuleFactory.cpp

## Purpose
Manages creation and registration of game modules (behaviors, updates, upgrades, etc.) for objects and drawables in the SAGE engine.

## Responsibilities
- Registers module templates via `addModule` calls
- Creates module instances from templates
- Handles module data serialization (CRC/xfer)
- Provides module lookup by name/type

## Key Types
- `ModuleFactory` (Class): Singleton factory for module creation
- `ModuleTemplate` (Struct): Template for module creation (proc, data proc, interface mask)
- `ModuleData` (Class): Base class for module configuration data

## Key Functions
### `init()`
- Purpose: Registers all module types with the factory
- Calls: `addModule` for each module type (behaviors, updates, upgrades, etc.)

### `newModule()`
- Purpose: Creates a new module instance from a template
- Calls: `findModuleTemplate()`, module-specific constructors

### `addModuleInternal()`
- Purpose: Adds a module template to the factory's registry
- Calls: None (direct map assignment)

### `findModuleTemplate()`
- Purpose: Looks up a module template by name and type
- Calls: `makeDecoratedNameKey()`

## Globals
- `TheModuleFactory` (ModuleFactory*): Singleton instance of the factory

## Dependencies
- Key includes: `Module.h`, `ModuleFactory.h`, `NameKeyGenerator.h`
- External symbols: `TheNameKeyGenerator`, `DEBUG_CRASH`, `DEBUG_ASSERTCRASH`
- Module types: Behavior, Update, Upgrade, Create, Die, Collide, Damage, Body, SpecialPower, ClientUpdate
