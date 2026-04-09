# Generals/Code/Libraries/Source/WWVegas/WWSaveLoad/persist.h

## Purpose
Defines the core interface for the game's save/load system, including the base `PersistClass` and associated factory/chunk classes.

## Responsibilities
- Declares the `PersistClass` interface for save/load operations.
- Defines abstract factory and chunk handler classes (`PersistFactoryClass`, `ChunkSaveClass`, `ChunkLoadClass`).
- Integrates with `PostLoadableClass` for post-load processing.

## Key Types
- **PersistClass (Class)**: Base interface for save/load capable objects.
- **PersistFactoryClass (Class)**: Maps chunk IDs to constructors/save/load functions.
- **ChunkSaveClass (Class)**: Handles saving chunks.
- **ChunkLoadClass (Class)**: Handles loading chunks.

## Key Functions
### PersistClass::Get_Factory
- Purpose: Returns the associated factory for this persistable object.
- Calls: None.

### PersistClass::Save
- Purpose: Saves the object's state to a chunk.
- Calls: None.

### PersistClass::Load
- Purpose: Loads the object's state from a chunk.
- Calls: None.

## Globals
- None.

## Dependencies
- `always.h`, `refcount.h`, `postloadable.h`
- `PostLoadableClass` (inherited by `PersistClass`)
