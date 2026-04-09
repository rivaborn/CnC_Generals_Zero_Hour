# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shddef.h

## Purpose
Defines base classes and enums for shader definitions in the SAGE engine, including versioning and shader capabilities.

## Responsibilities
- Declares `ShdDefClass` as the base class for shader definitions
- Defines shader version enum (`SHDVER`)
- Provides abstract factory pattern for shader creation
- Manages shader metadata (name, surface type, requirements)

## Key Types
- `ShdInterfaceClass` (Class): Not defined here; referenced as shader interface
- `SHDVER` (Enum): Shader version constants (undefined, 6, 7, 8)
- `ShdVersion` (Class): Wrapper for shader version with getter/setter
- `ShdDefClass` (Class): Base class for shader definitions with editable/refcounted properties

## Key Functions
### `ShdDefClass::Create`
- Purpose: Abstract factory to create hardware-compatible shader instances
- Calls: None (pure virtual)

### `ShdDefClass::Is_Valid_Config`
- Purpose: Validates shader configuration
- Calls: None

### `ShdDefClass::Save`/`Load`
- Purpose: Persistence methods for shader definitions
- Calls: `Save_Variables`, `Load_Variables`

## Globals
- None

## Dependencies
- `always.h`, `editable.h`, `refcount.h`
- `StringClass`, `ChunkSaveClass`, `ChunkLoadClass`
- `DECLARE_EDITABLE` macro
