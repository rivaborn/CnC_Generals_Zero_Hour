# Generals/Code/Libraries/Source/WWVegas/WWSaveLoad/definitionmgr.h

## Purpose
Manages game definitions (e.g., units, buildings) for save/load functionality in the SAGE engine.

## Responsibilities
- Registers/unregisters definitions
- Provides lookup methods (by ID, name, type)
- Handles save/load persistence for definitions
- Enumerates definitions via sorted array

## Key Types
- **DefinitionMgrClass (Class)**: Central manager for game definitions
- **DefinitionClass (Class)**: Base class for game definitions (forward declared)
- **ID_TYPE (Enum)**: Identifies lookup type (class/superclass)

## Key Functions
### `Register_Definition`
- Purpose: Adds a definition to the manager
- Calls: Not visible in header

### `Find_Definition`
- Purpose: Retrieves a definition by ID
- Calls: Not visible in header

### `Save_Objects`
- Purpose: Serializes definitions for save
- Calls: Not visible in header

## Globals
- **_TheDefinitionMgr (DefinitionMgrClass)**: Singleton instance
- **DefinitionHash (HashTemplateClass)**: Internal hash for definitions

## Dependencies
- `saveload.h`, `saveloadsubsystem.h`, `wwstring.h`, `hashtemplate.h`
- `SaveLoadSubSystemClass` (inheritance)
- `ChunkSaveClass`, `ChunkLoadClass` (save/load)
