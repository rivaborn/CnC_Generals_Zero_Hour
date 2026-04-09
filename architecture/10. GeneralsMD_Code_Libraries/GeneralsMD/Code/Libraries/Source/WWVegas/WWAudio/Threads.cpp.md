# GeneralsMD/Code/Libraries/Source/WWVegas/WWAudio/Threads.cpp

## Purpose
Manages delayed object release via a background thread for audio resources.

## Responsibilities
- Creates and manages a delayed release thread
- Adds objects to a delayed release queue
- Flushes or releases objects when their delay expires
- Handles thread shutdown gracefully

## Key Types
- `WWAudioThreadsClass` (Class): Manages delayed object release threading
- `DELAYED_RELEASE_INFO` (Struct): Holds object and timing info for delayed release

## Key Functions
### `Create_Delayed_Release_Thread`
- Purpose: Starts the background thread if not already running
- Calls: `_beginthread`, `CreateEvent`

### `End_Delayed_Release_Thread`
- Purpose: Stops the background thread and cleans up resources
- Calls: `SetEvent`, `WaitForSingleObject`

### `Add_Delayed_Release_Object`
- Purpose: Queues an object for delayed release
- Calls: `Create_Delayed_Release_Thread`, `GetTickCount`

### `Flush_Delayed_Release_Objects`
- Purpose: Immediately releases all queued objects
- Calls: `REF_PTR_RELEASE`, `SAFE_DELETE`

### `Delayed_Release_Thread_Proc`
- Purpose: Background thread that processes delayed releases
- Calls: `WaitForSingleObject`, `GetTickCount`, `REF_PTR_RELEASE`, `SAFE_DELETE`

## Globals
- `m_ReleaseListHead` (DELAYED_RELEASE_INFO*): Head of delayed release queue
- `m_ListMutex` (CriticalSectionClass): Protects access to release list
- `m_hDelayedReleaseThread` (HANDLE): Handle to background thread
- `m_hDelayedReleaseEvent` (HANDLE): Event to signal thread shutdown
- `m_CriticalSection` (CriticalSectionClass): General thread synchronization
- `m_IsShuttingDown` (bool): Flag indicating shutdown state

## Dependencies
- `Threads.h`, `refcount.h`, `Utils.h`, `<Process.h>`, `wwdebug.h`
- `RefCountClass`, `CriticalSectionClass`, `W3DNEW`, `REF_PTR_RELEASE`, `SAFE_DELETE`
- Windows API: `CreateEvent`, `_beginthread`, `WaitForSingleObject`, `SetEvent`, `GetTickCount`
