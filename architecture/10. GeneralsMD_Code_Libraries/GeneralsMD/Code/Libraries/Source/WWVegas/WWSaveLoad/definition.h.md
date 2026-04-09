# GeneralsMD/Code/Libraries/Source/WWVegas/WWSaveLoad/definition.h

## Purpose
Defines the base `DefinitionClass` for game object definitions, supporting persistence, editing, and identification.

## Responsibilities
- Provides core interface for game definitions (ID, name, persistence)
- Manages save/load functionality via chunk-based serialization
- Supports editable properties and user data
- Acts as base class for specific definition types

## Key Types
- **DefinitionClass (Class)**: Base class for game object definitions.
- **ChunkSaveClass (Class)**: Forward-declared save interface.
- **ChunkLoadClass (Class)**: Forward-declared load interface.

## Key Functions
### `Get_Class_ID`
- Purpose: Returns the class ID (pure virtual).
- Calls: None.

### `Save`
- Purpose: Saves object state to a chunk.
- Calls: `Save_Variables`.

### `Load`
- Purpose: Loads object state from a chunk.
- Calls: `Load_Variables`.

### `Is_Valid_Config`
- Purpose: Validates object configuration (default: always valid).
- Calls: None.

## Globals
- None.

## Dependencies
- `always.h`, `definitionclassids.h`, `definitionmgr.h`, `editable.h`, `wwstring.h`
- `PersistClass`, `EditableClass` (inherited)
- `StringClass` (member variable type)
