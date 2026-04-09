# GeneralsMD/Code/Libraries/Source/WWVegas/WWSaveLoad/saveload.cpp

## Purpose
Handles game save/load functionality, including subsystem registration, pointer remapping, and post-load processing.

## Responsibilities
- Manages save/load subsystems and factories
- Handles pointer remapping during load
- Processes post-load callbacks
- Provides chunk-based save/load operations

## Key Types
- SaveLoadSystemClass (Class): Core save/load manager
- SaveLoadSubSystemClass (Class): Base class for saveable subsystems
- PersistFactoryClass (Class): Factory for creating persistable objects
- PointerRemapClass (Class): Handles pointer remapping during load
- PostLoadableClass (Class): Interface for objects needing post-load processing

## Key Functions
### SaveLoadSystemClass::Save
- Purpose: Saves a subsystem's data to a chunk
- Calls: ChunkSaveClass::Begin_Chunk, ChunkSaveClass::End_Chunk, subsystem.Save

### SaveLoadSystemClass::Load
- Purpose: Loads all subsystems from a chunk stream
- Calls: ChunkLoadClass::Open_Chunk, Find_Sub_System, PointerRemapper.Process, Post_Load_Processing

### SaveLoadSystemClass::Post_Load_Processing
- Purpose: Executes post-load callbacks for registered objects
- Calls: PostLoadList.Remove_Head, obj.On_Post_Load

### SaveLoadSystemClass::Register_Pointer
- Purpose: Registers a pointer for remapping during load
- Calls: PointerRemapper.Register_Pointer

### Force_Link_WWSaveLoad
- Purpose: Forces linking of save/load code (likely for static linking)
- Calls: FORCE_LINK

## Globals
- SubSystemListHead (SaveLoadSubSystemClass*): Head of registered subsystems
- FactoryListHead (PersistFactoryClass*): Head of registered factories
- PostLoadList (SList<PostLoadableClass>): List of objects needing post-load processing
- PointerRemapper (PointerRemapClass): Global pointer remapper instance

## Dependencies
- saveload.h, saveloadsubsystem.h, persist.h, persistfactory.h, chunkio.h, wwdebug.h, saveloadstatus.h, wwhack.h, wwprofile.h
- windows.h, systimer.h
- WWLOG, WWASSERT, TIMEGETTIME macros
- ChunkSaveClass, ChunkLoadClass, RefCountClass, SList, SLNode classes
