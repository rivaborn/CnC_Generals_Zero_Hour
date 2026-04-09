# Generals/Code/Libraries/Source/WWVegas/WWAudio/Threads.cpp

## Purpose
Manages delayed object release via a background thread to prevent immediate memory deallocation.

## Responsibilities
- Creates and manages a background thread for delayed object release
- Adds objects to a delayed release queue with configurable delay
- Flushes all pending delayed releases
- Handles thread shutdown gracefully

## Key Types
- `WWAudioThreadsClass` (Class): Manages delayed object release threading
- `DELAYED_RELEASE_INFO` (Struct): Contains object reference and release timing info

## Key Functions
### `Create_Delayed_Release_Thread`
- Purpose: Creates the background thread if not already running
- Calls: `_beginthread`, `CreateEvent`

### `End_Delayed_Release_Thread`
- Purpose: Signals thread to stop and waits for completion
- Calls: `SetEvent`, `WaitForSingleObject`

### `Add_Delayed_Release_Object`
- Purpose: Adds an object to the delayed release queue
- Calls: `Create_Delayed_Release_Thread`, `GetTickCount`

### `Flush_Delayed_Release_Objects`
- Purpose: Immediately releases all pending delayed objects
- Calls: `REF_PTR_RELEASE`, `SAFE_DELETE`

### `Delayed_Release_Thread_Proc`
- Purpose: Background thread procedure that processes delayed releases
- Calls: `WaitForSingleObject`, `GetTickCount`, `REF_PTR_RELEASE`, `SAFE_DELETE`

## Globals
- `m_ReleaseListHead` (DELAYED_RELEASE_INFO*): Head of delayed release list
- `m_ListMutex` (CriticalSectionClass): Protects access to release list
- `m_hDelayedReleaseThread` (HANDLE): Handle to background thread
- `m_hDelayedReleaseEvent` (HANDLE): Event for thread signaling
- `m_CriticalSection` (CriticalSectionClass): General thread synchronization
- `m_IsShuttingDown` (bool): Shutdown flag

## Dependencies
- `Threads.h`, `refcount.h`, `Utils.h`, `<Process.h>`, `wwdebug.h`
- `RefCountClass`, `CriticalSectionClass`, `W3DNEW`, `REF_PTR_RELEASE`, `SAFE_DELETE`
