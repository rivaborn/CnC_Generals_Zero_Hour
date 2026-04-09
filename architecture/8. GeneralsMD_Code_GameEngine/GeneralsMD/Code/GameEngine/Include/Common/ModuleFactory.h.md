# GeneralsMD/Code/GameEngine/Include/Common/ModuleFactory.h

## Purpose
Defines the `ModuleFactory` class, a singleton subsystem for creating and managing game modules (e.g., UpdateModule, DamageModule) attached to game objects and drawables.

## Responsibilities
- Registers module templates via `addModuleInternal`.
- Creates new modules (`newModule`) and module data (`newModuleDataFromINI`) at runtime.
- Manages module templates in a map (`m_moduleTemplateMap`) and module data in a list (`m_moduleDataList`).
- Supports serialization via `crc`, `xfer`, and `loadPostProcess`.

## Key Types
- **ModuleFactory (Class)**: Singleton factory for creating game modules.
- **ModuleTemplate (Class)**: Stores creation callbacks (`m_createProc`, `m_createDataProc`) and interface mask for a module type.
- **ModuleTemplateMap (Type)**: `std::map` of `NameKeyType` to `ModuleTemplate` for template lookup.
- **ModuleDataList (Type)**: `std::vector` of `const ModuleData*` for storing module data.
- **NewModuleProc (Type)**: Callback to create a `Module` from a `Thing` and `ModuleData`.
- **NewModuleDataProc (Type)**: Callback to create `ModuleData` from an `INI` file.

## Key Functions
### `newModule`
- Purpose: Creates a new module of the specified type for a given `Thing`.
- Calls: `findModuleTemplate`, `m_createProc`.

### `newModuleDataFromINI`
- Purpose: Creates module data from an INI file.
- Calls: `m_createDataProc`.

### `addModuleInternal`
- Purpose: Registers a new module template with the factory.
- Calls: None (directly modifies `m_moduleTemplateMap`).

### `findModuleTemplate`
- Purpose
