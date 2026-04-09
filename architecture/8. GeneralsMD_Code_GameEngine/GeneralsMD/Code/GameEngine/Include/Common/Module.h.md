# GeneralsMD/Code/GameEngine/Include/Common/Module.h

## Purpose
Defines the module system for the SAGE engine, including base classes for object and drawable modules, their data, and related enums.

## Responsibilities
- Declares module hierarchy (Module, ObjectModule, DrawableModule)
- Defines module types and interface types
- Provides macros for standard module implementation
- Declares ModuleData base class for INI-based module data

## Key Types
- **TimeOfDay (Enum)**: Not inferable.
- **StaticGameLODLevel (Enum)**: Not inferable.
- **ModuleType (Enum)**: Categorizes module types (behavior, draw, client update).
- **ModuleInterfaceType (Enum)**: Bit flags for module interface capabilities.
- **ModuleData (Class)**: Base class for module data read from INI files.
- **Module (Class)**: Base class for all modules (object/drawable).
- **ObjectModule (Class)**: Module interface specific to Objects.
- **DrawableModule (Class)**: Module interface specific to Drawables.

## Key Functions
### `Module::onObjectCreated()`
- Purpose: Allows modules to resolve inter-module dependencies after creation.
- Calls: None visible.

### `Module::onDrawableBoundToObject()`
- Purpose: Called when a drawable is bound to an object.
- Calls: None visible.

### `Module::preloadAssets(TimeOfDay)`
- Purpose: Preloads assets for a specific time of day.
- Calls: None visible.

### `ObjectModule::onCapture(Player*, Player*)`
- Purpose: Called when an object changes ownership.
- Calls: None visible.

### `ObjectModule::onDisabledEdge(Bool)`
- Purpose: Called when object's disabled state changes.
- Calls: None visible.

## Globals
- None.

## Dependencies
- `Common/INI.h`, `Common/GameMemory.h`, `Common/NameKeyGenerator.h`, `Common/Snapshot.h`
- Forward references: `Drawable`, `Object`, `Player`, `Thing`, `W3DModelDrawModuleData`, `W3DTreeDrawModuleData`, `FieldParse`
