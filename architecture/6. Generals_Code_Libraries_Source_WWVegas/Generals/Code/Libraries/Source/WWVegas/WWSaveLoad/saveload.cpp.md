# Generals/Code/Libraries/Source/WWVegas/WWSaveLoad/saveload.cpp

## Purpose
Manages game save/load functionality, including subsystem registration, pointer remapping, and post-load processing.

## Responsibilities
- Registers/unregisters save/load subsystems and factories
- Handles chunk-based save/load operations
- Manages pointer remapping during load
- Processes post-load callbacks

## Key Types
- **SaveLoadSystemClass**: Core save/load manager
- **SaveLoadSubSystemClass**: Base class for saveable subsystems
- **PersistFactoryClass**: Factory for creating persistable objects
- **PostLoadableClass**: Interface for objects needing post-load processing
- **PointerRemapClass**: Handles pointer remapping during load

## Key Functions
### Save
- Purpose: Saves a subsystem's data to a chunk
- Calls: `Begin_Chunk`, `End_Chunk`, subsystem's `Save`

### Load
- Purpose: Loads all chunks and processes pointer remaps
- Calls: `Open_Chunk`, `Close_Chunk`, `Find_Sub_System`, `PointerRemapper.Process`

### Post_Load_Processing
- Purpose: Executes post-load callbacks for registered objects
- Calls: `Remove_Head`, `On_Post_Load`

### Register_Pointer
- Purpose: Registers a pointer for remapping
- Calls: `PointerRemapper.Register_Pointer`

## Globals
- **SubSystemListHead** (SaveLoadSubSystemClass*): Head of subsystem list
- **FactoryListHead** (PersistFactoryClass*): Head of factory list
- **PostLoadList** (SList<PostLoadableClass>): List of post-load callbacks
- **PointerRemapper** (PointerRemapClass): Handles pointer remapping

## Dependencies
- `saveload.h`, `saveloadsubsystem.h`, `persist.h`, `persistfactory.h`, `chunkio.h`, `wwdebug.h`, `saveloadstatus.h`, `wwhack.h`
- `ChunkSaveClass`, `ChunkLoadClass`, `RefCountClass`, `SLNode`
