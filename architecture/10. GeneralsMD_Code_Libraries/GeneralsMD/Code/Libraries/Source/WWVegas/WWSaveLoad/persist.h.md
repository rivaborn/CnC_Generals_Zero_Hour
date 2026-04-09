# GeneralsMD/Code/Libraries/Source/WWVegas/WWSaveLoad/persist.h

## Purpose
Defines the core interface for the game's save/load system, including the base `PersistClass` and associated factory/chunk classes.

## Responsibilities
- Declares the `PersistClass` interface for save/load operations.
- Defines abstract methods for factory access, saving, and loading.
- References `PersistFactoryClass`, `ChunkSaveClass`, and `ChunkLoadClass` for concrete implementations.
- Inherits from `PostLoadableClass` for post-load processing.

## Key Types
- **PersistClass (Class)**: Base interface for save/load-capable objects.
- **PersistFactoryClass (Class)**: Factory for mapping chunk IDs to constructors/save/load functions.
- **ChunkSaveClass (Class)**: Handler for saving object data.
- **ChunkLoadClass (Class)**: Handler for loading object data.

## Key Functions
### PersistClass::Get_Factory
- Purpose: Returns the associated factory for this persistable object.
- Calls: None.

### PersistClass::Save
- Purpose: Saves the object's state to a chunk.
- Calls: None (default implementation returns `true`).

### PersistClass::Load
- Purpose: Loads the object's state from a chunk.
- Calls: None (default implementation returns `true`).

## Globals
- None.

## Dependencies
- `always.h`, `refcount.h`, `postloadable.h`
- `PostLoadableClass` (inherited)
