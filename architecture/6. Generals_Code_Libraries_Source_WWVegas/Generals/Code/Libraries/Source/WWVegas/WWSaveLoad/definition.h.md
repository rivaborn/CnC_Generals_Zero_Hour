# Generals/Code/Libraries/Source/WWVegas/WWSaveLoad/definition.h

## Purpose
Defines the base `DefinitionClass` for game object definitions, supporting serialization and management.

## Responsibilities
- Provides core interface for game definitions (ID, name, save/load)
- Manages user data and save enable/disable flags
- Supports validation and persistence via `ChunkSaveClass`/`ChunkLoadClass`
- Integrates with `DefinitionMgrClass` for object management

## Key Types
- **DefinitionClass (Class)**: Base class for game object definitions.
- **ChunkSaveClass (Class)**: Forward-declared save interface (not defined here).
- **ChunkLoadClass (Class)**: Forward-declared load interface (not defined here).

## Key Functions
### `Get_Name()`
- Purpose: Returns the definition's display name.
- Calls: None.

### `Set_Name()`
- Purpose: Sets the definition's display name.
- Calls: None.

### `Get_ID()`
- Purpose: Returns the definition's numeric ID.
- Calls: None.

### `Set_ID()`
- Purpose: Sets the definition's numeric ID.
- Calls: None.

### `Is_Valid_Config()`
- Purpose: Validates the definition's configuration (default: always valid).
- Calls: None.

### `Save_Variables()`
- Purpose: Serializes private member variables.
- Calls: `ChunkSaveClass` methods (not visible in header).

### `Load_Variables()`
- Purpose: Deserializes private member variables.
- Calls: `ChunkLoadClass` methods (not visible in header).

## Globals
- **None**.

## Dependencies
- `always.h`, `definitionmgr.h`, `editable.h`, `wwstring.h`
- `ChunkSaveClass`, `ChunkLoadClass` (forward-declared)
- Inher
