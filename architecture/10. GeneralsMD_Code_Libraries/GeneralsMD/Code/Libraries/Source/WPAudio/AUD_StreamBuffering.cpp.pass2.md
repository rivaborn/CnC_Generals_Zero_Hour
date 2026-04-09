# GeneralsMD/Code/Libraries/Source/WPAudio/AUD_StreamBuffering.cpp - Enhanced Analysis

## Architectural Role
This file implements the core audio streaming infrastructure for the SAGE engine, managing circular buffers for audio data with multiple concurrent accessors. It bridges the low-level file I/O subsystem (`wsys/file.h`) with higher-level audio playback systems, enabling efficient streaming of large audio files without full memory loading.

## Cross-References
### Incoming
- Audio playback systems (likely in `WPAudio` subsystem) call `STM_AccessAdvance` and `STM_AccessGetBlock` for stream data retrieval
- Memory management systems call `STM_StreamCreate`/`STM_StreamDestroy` for stream lifecycle
- Debug profiling systems use `STM_Profile*` functions for performance monitoring

### Outgoing
- Calls into `wsys/file.h` for file operations (not shown in truncated content but implied by file I/O patterns)
- Uses `MEM_ALLOC_STRUCT`/`MEM_Free` from memory subsystem
- Depends on `AudioGetTime()` from timing subsystem (for profiling)

## Design Patterns
- **Circular Buffer**: Implements a linked-list based circular buffer system for efficient streaming
- **Reference Counting**: Uses `STM_ACCESS::ref` for managing accessor lifetimes
- **Factory Pattern**: `STM_StreamCreate`/`STM_StreamDestroy` pair for object creation/destruction

*Not inferable*: Exact synchronization mechanism between accessors (likely mutexes or critical sections not shown in truncated content)
