# Generals/Code/Libraries/Source/WWVegas/WWSaveLoad/twiddler.h

## Purpose
Defines the `TwiddlerClass`, a persistence class for managing indirect class references in save/load operations.

## Responsibilities
- Manages indirect class ID references for save/load operations
- Provides persistence methods (Save/Load)
- Supports dynamic definition lists
- Implements the `Twiddle` interface for object manipulation

## Key Types
- **TwiddlerClass (Class)**: Persistence class handling indirect class references and dynamic definitions

## Key Functions
### `TwiddlerClass::Twiddle`
- Purpose: Creates a new instance of the referenced class
- Calls: `Create`

### `TwiddlerClass::Save`
- Purpose: Saves object state to a chunk save stream
- Calls: `Save_Variables`

### `TwiddlerClass::Load`
- Purpose: Loads object state from a chunk load stream
- Calls: `Load_Variables`

### `TwiddlerClass::Get_Indirect_Class_ID`
- Purpose: Returns the stored indirect class ID
- Calls: None

### `TwiddlerClass::Set_Indirect_Class_ID`
- Purpose: Sets the indirect class ID
- Calls: None

## Globals
- None

## Dependencies
- `definition.h`
- `definitionclassids.h`
- `DefinitionClass`
- `PersistClass`
- `ChunkSaveClass`
- `ChunkLoadClass`
- `PersistFactoryClass`
- `DynamicVectorClass`
