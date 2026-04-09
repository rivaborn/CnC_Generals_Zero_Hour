# GeneralsMD/Code/Libraries/Source/WWVegas/WWAudio/Threads.h

## Purpose
Defines the `WWAudioThreadsClass` for managing audio-related threads, particularly for delayed object release.

## Responsibilities
- Manages a delayed release thread for safe object cleanup
- Provides thread synchronization mechanisms
- Handles delayed release of `RefCountClass` objects
- Manages thread shutdown and event signaling

## Key Types
- `RefCountClass` (Class): Reference-counted object base class
- `WWAudioThreadsClass` (Class): Thread management for audio subsystem
- `_DELAYED_RELEASE_INFO` (Struct): Linked list node for delayed release objects
- `DELAYED_RELEASE_INFO` (Struct): Alias for `_DELAYED_RELEASE_INFO`

## Key Functions
### `Create_Delayed_Release_Thread`
- Purpose: Creates and starts the delayed release thread
- Calls: Not inferable

### `End_Delayed_Release_Thread`
- Purpose: Stops the delayed release thread with timeout
- Calls: Not inferable

### `Add_Delayed_Release_Object`
- Purpose: Adds an object to the delayed release queue
- Calls: Not inferable

### `Flush_Delayed_Release_Objects`
- Purpose: Immediately releases all pending objects
- Calls: Not inferable

### `Delayed_Release_Thread_Proc`
- Purpose: Thread procedure that processes delayed releases
- Calls: Not inferable

## Globals
- `m_hDelayedReleaseThread` (HANDLE): Handle to the delayed release thread
- `m_hDelayedReleaseEvent` (HANDLE): Event for thread synchronization
- `m_CriticalSection` (CriticalSectionClass): Thread synchronization
- `m_ReleaseListHead` (DELAYED_RELEASE_INFO*): Head of delayed release list
