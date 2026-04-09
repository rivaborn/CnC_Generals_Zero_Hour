# GeneralsMD/Code/Libraries/Source/WWVegas/WWSaveLoad/saveload.h

## Purpose
Header file defining the core save/load system framework for the game, including object persistence, pointer remapping, and chunk-based file I/O.

## Responsibilities
- Declares the `SaveLoadSystemClass` and related abstract classes/interfaces
- Defines the save/load architecture (subsystems, factories, chunks, pointer remapping)
- Provides macros for debug-enabled pointer remapping
- Manages registration of subsystems and factories

## Key Types
- **RefCountClass (Class)**: Reference-counted object base class
- **SaveLoadSubSystemClass (Class)**: Abstract base for save/load subsystems
- **PersistFactoryClass (Class)**: Abstract factory for creating persistent objects
- **PersistClass (Class)**: Abstract interface for persistent objects
- **PostLoadableClass (Class)**: Interface for objects needing post-load callbacks
- **ChunkSaveClass (Class)**: Abstract chunk-based save interface
- **ChunkLoadClass (Class)**: Abstract chunk-based load interface
- **SaveLoadSystemClass (Class)**: Core save/load system manager

## Key Functions
### SaveLoadSystemClass::Save
- Purpose: Save a subsystem's data to a chunk stream
- Calls: `ChunkSaveClass` methods

### SaveLoadSystemClass::Load
- Purpose: Load data from a chunk stream and optionally process post-load callbacks
- Calls: `ChunkLoadClass` methods, `Post_Load_Processing`

### SaveLoadSystemClass::Post_Load_Processing
- Purpose: Execute registered post-load callbacks after pointer remapping
- Calls: Callback functions registered via `Register_Post_Load_Callback`

### SaveLoadSystemClass::Find_Persist_Factory
- Purpose: Look up a factory by chunk ID
- Calls: None (uses internal linked list)

### SaveLoadSystemClass::Register_Post_Load_Callback
- Purpose: Register an object for post-load processing
- Calls: None (adds to `PostLoadList`)

### SaveLoadSystemClass::Request_Pointer_Remap
- Purpose: Request remapping of a pointer after loading
- Calls: `PointerRemapper` methods

## Globals
- **SubSystemListHead (SaveLoadSubSystemClass*)**: Head of registered subsystems list
- **FactoryListHead (PersistFactoryClass*)**: Head of registered factories list
- **PointerRemapper (PointerRemapClass)**: Manages pointer remapping during load
- **PostLoadList (SList<PostLoadableClass>)**: List of objects needing post-load callbacks

## Dependencies
- `always.h`, `pointerremap.h`, `bittype.h`, `slist.h`
- `RefCountClass`, `SaveLoadSubSystemClass`,
