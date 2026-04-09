# GeneralsMD/Code/Libraries/Source/WPAudio/AUD_Memory.cpp

## Purpose
Manages memory pools for audio system, including allocation, deallocation, and path string utilities.

## Responsibilities
- Creates and destroys memory pools for audio data
- Allocates and returns memory items from pools
- Tracks pool usage statistics
- Provides path string manipulation utilities

## Key Types
- AudioMemoryPool (struct): Memory pool container
- MemoryItem (struct): Linked list node for memory items

## Key Functions
### MemoryPoolCreate
- Purpose: Creates a new memory pool with specified items and size
- Calls: AudioMemAlloc

### MemoryPoolDestroy
- Purpose: Destroys a memory pool and frees its memory
- Calls: AudioMemFree

### MemoryPoolGetItem
- Purpose: Retrieves an available memory item from the pool
- Calls: None

### MemoryPoolReturnItem
- Purpose: Returns a memory item back to the pool
- Calls: None

### MemoryPoolCount
- Purpose: Counts available items in the pool
- Calls: None

### AudioAddSlash
- Purpose: Ensures a path string ends with a backslash
- Calls: strlen, strchr

### AudioHasPath
- Purpose: Checks if a string contains path characters
- Calls: strchr

## Globals
- AudioMemoryPool (struct): Memory pool structure definition
- MemoryItem (struct): Memory item structure definition

## Dependencies
- <string.h> for string operations
- <wpaudio/altypes.h> for audio types
- <wpaudio/memory.h> for memory allocation
- DBG_* macros for debugging
- AudioMemAlloc/AudioMemFree for memory management
