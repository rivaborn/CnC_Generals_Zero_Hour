# GeneralsMD/Code/Libraries/Source/WPAudio/AUD_StreamBuffering.cpp

## Purpose
Manages audio stream buffering, including stream creation/destruction, buffer management, and access control for audio data.

## Responsibilities
- Stream lifecycle management (create/destroy/reset)
- Buffer management (creation, destruction, linking)
- Access control for multiple accessors (read/write)
- Position tracking and data transfer
- Error handling and state management

## Key Types
- `STM_STREAM`: Main stream structure containing buffers and accessors
- `STM_SBUFFER`: Stream buffer structure holding audio data regions
- `STM_ACCESS`: Access interface for reading/writing stream data
- `STM_REGION`: Data region within a buffer for specific accessors

## Key Functions
### `STM_StreamCreate`
- Purpose: Creates and initializes a new audio stream
- Calls: `STM_stream_init`, `MEM_ALLOC_STRUCT`

### `STM_StreamDestroy`
- Purpose: Destroys a stream and its buffers
- Calls: `STM_StreamDestroyBuffers`, `MEM_Free`

### `STM_AccessUpdate`
- Purpose: Updates accessor position and notifies upstream accessor
- Calls: `STM_AccessUpStreamAccessor`, `STM_next_sbuffer`, `STM_AccessReturnToStart`

### `STM_AccessAdvance`
- Purpose: Advances accessor position in the stream
- Calls: `STM_AccessTotalBytes`, `STM_next_sbuffer`, `STM_AccessUpdate`

### `STM_AccessGetBlock`
- Purpose: Retrieves current block of data for accessor
- Calls: `STM_AccessAdvance`

## Globals
- `STM_SBUFFER` (Type): Debug type declaration for stream buffers
- `STM_ACCESS` (Type): Debug type declaration for access interfaces
- `STM_STREAM` (Type): Debug type declaration for streams

## Dependencies
- `<wpaudio/StreamBuffering.h>`: Core stream buffering definitions
- `<wpaudio/list.h>`: Linked list utilities
- `<wpaudio/memory.h>`: Memory allocation functions
- `<wsys/file.h>`: File system utilities
- `AudioGetTime()`: Time measurement for profiling
