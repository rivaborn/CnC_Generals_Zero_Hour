# GeneralsMD/Code/Libraries/Source/WWVegas/WWSaveLoad/saveloadsubsystem.h

## Purpose
Defines the base class for save/load subsystems in the game's save system.

## Responsibilities
- Provides abstract interface for save/load operations
- Manages registration with the global SaveLoadSystem
- Defines chunk-based save/load architecture

## Key Types
- **SaveLoadSubSystemClass (Class)**: Abstract base class for save/load subsystems
- **ChunkLoadClass (Class)**: Forward declaration for load chunk handler
- **ChunkSaveClass (Class)**: Forward declaration for save chunk handler

## Key Functions
### SaveLoadSubSystemClass()
- Purpose: Constructor for the save/load subsystem
- Calls: Not inferable

### ~SaveLoadSubSystemClass()
- Purpose: Destructor for the save/load subsystem
- Calls: Not inferable

### Chunk_ID()
- Purpose: Returns the unique chunk ID for this subsystem
- Calls: Not inferable

### Save()
- Purpose: Abstract method to save subsystem data
- Calls: Not inferable

### Load()
- Purpose: Abstract method to load subsystem data
- Calls: Not inferable

### Name()
- Purpose: Returns the name of this subsystem
- Calls: Not inferable

## Globals
- **NextSubSystem (SaveLoadSubSystemClass*)**: Private link to next subsystem (managed by SaveLoadSystem)

## Dependencies
- `always.h`, `bittype.h`, `postloadable.h`
- `PostLoadableClass` (inheritance)
- `ChunkLoadClass`, `ChunkSaveClass` (forward declarations)
