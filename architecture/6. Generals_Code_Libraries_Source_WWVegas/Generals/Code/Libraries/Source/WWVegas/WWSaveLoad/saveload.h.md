# Generals/Code/Libraries/Source/WWVegas/WWSaveLoad/saveload.h

## Purpose
Defines the core save/load system framework for the game, including object persistence, pointer remapping, and chunk-based file handling.

## Responsibilities
- Manages save/load operations for game state
- Handles object persistence and factory registration
- Implements pointer remapping during load
- Coordinates post-load processing callbacks
- Maintains subsystem and factory registries

## Key Types
- **RefCountClass (Class)**: Reference-counted object base class
- **SaveLoadSubSystemClass (Class)**: Base class for save/load subsystems
- **PersistFactoryClass (Class)**: Abstract factory for persistent objects
- **PersistClass (Class)**: Base interface for saveable objects
- **PostLoadableClass (Class)**: Interface for objects needing post-load processing
- **ChunkSaveClass (Class)**: Chunk-based save interface
- **ChunkLoadClass (Class)**: Chunk-based load interface
- **SaveLoadSystemClass (Class)**: Core save/load system manager

## Key Functions
### SaveLoadSystemClass::Save
- Purpose: Saves a subsystem's data to a chunk stream
- Calls: ChunkSaveClass methods

### SaveLoadSystemClass::Load
- Purpose: Loads data from a chunk stream
- Calls: ChunkLoadClass methods, Post_Load_Processing

### SaveLoadSystemClass::Post_Load_Processing
- Purpose: Executes post-load callbacks after pointer remapping
- Calls: PostLoadableClass callbacks

### SaveLoadSystemClass::Request_Pointer_Remap
- Purpose: Registers a pointer for remapping during load
- Calls: PointerRemapClass methods

### SaveLoadSystemClass::Register_Post_Load_Callback
- Purpose: Registers an object for post-load processing
- Calls: SList methods

## Globals
- **SubSystemListHead (SaveLoadSubSystemClass*)**: Head of registered subsystems
- **FactoryListHead (PersistFactoryClass*)**: Head of registered factories
- **PointerRemapper (PointerRemapClass)**: Handles pointer remapping
- **PostLoadList (SList<PostLoadableClass>)**: List of post-load callbacks

## Dependencies
- `always.h`, `pointerremap.h`, `bittype.h`, `slist.h`
- `RefCountClass`, `SaveLoadSubSystemClass`, `PersistFactoryClass`, `PersistClass`, `PostLoadableClass`, `ChunkSaveClass`, `ChunkLoadClass`
