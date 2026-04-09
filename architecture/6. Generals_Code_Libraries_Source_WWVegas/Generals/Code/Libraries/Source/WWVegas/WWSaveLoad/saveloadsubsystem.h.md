# Generals/Code/Libraries/Source/WWVegas/WWSaveLoad/saveloadsubsystem.h

## Purpose
Defines the base class for save/load subsystems in the game's save system.

## Responsibilities
- Provides abstract interface for save/load operations
- Manages registration with the global SaveLoadSystem
- Defines chunk ID and naming conventions for subsystems

## Key Types
- **SaveLoadSubSystemClass (Class)**: Abstract base class for save/load subsystems
- **ChunkLoadClass (Class)**: Forward declaration (loading interface)
- **ChunkSaveClass (Class)**: Forward declaration (saving interface)

## Key Functions
### SaveLoadSubSystemClass()
- Purpose: Constructor for the base save/load subsystem class
- Calls: None

### ~SaveLoadSubSystemClass()
- Purpose: Virtual destructor for the base save/load subsystem class
- Calls: None

### Chunk_ID()
- Purpose: Returns the unique chunk ID for this subsystem
- Calls: None

### Contains_Data()
- Purpose: Indicates whether this subsystem contains data to save
- Calls: None

### Save()
- Purpose: Saves subsystem data to a chunk
- Calls: None

### Load()
- Purpose: Loads subsystem data from a chunk
- Calls: None

### Name()
- Purpose: Returns the name of this subsystem
- Calls: None

## Globals
- **NextSubSystem (SaveLoadSubSystemClass*)**: Link to next subsystem (managed by SaveLoadSystem)

## Dependencies
- `always.h`, `bittype.h`, `postloadable.h`
- `PostLoadableClass` (inheritance)
- `ChunkLoadClass`, `ChunkSaveClass` (forward declarations)
