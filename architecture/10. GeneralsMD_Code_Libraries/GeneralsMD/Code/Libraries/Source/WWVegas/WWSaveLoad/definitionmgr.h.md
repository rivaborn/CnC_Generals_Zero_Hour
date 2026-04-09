# GeneralsMD/Code/Libraries/Source/WWVegas/WWSaveLoad/definitionmgr.h

## Purpose
Manages game definitions (e.g., units, buildings) for save/load and runtime access.

## Responsibilities
- Registers/unregisters definitions
- Provides lookup by ID, name, or type
- Handles save/load persistence
- Enumerates definitions

## Key Types
- **DefinitionMgrClass (Class)**: Manages definition registry and persistence
- **DefinitionClass (Class)**: Base class for game definitions (forward-declared)
- **ID_TYPE (Enum)**: Identifies lookup type (class/superclass)

## Key Functions
### `Register_Definition`
- Purpose: Adds a definition to the manager
- Calls: HashTemplateClass operations

### `Find_Definition`
- Purpose: Retrieves a definition by ID
- Calls: HashTemplateClass lookup

### `Save/Load`
- Purpose: Persists definitions to/from save files
- Calls: `Save_Objects`, `Save_Variables`, etc.

## Globals
- `_TheDefinitionMgr (DefinitionMgrClass)`: Singleton instance
- `DefinitionHash (HashTemplateClass)`: Stores definitions by name

## Dependencies
- `saveload.h`, `saveloadsubsystem.h`, `wwstring.h`
- `HashTemplateClass`, `DynamicVectorClass`
