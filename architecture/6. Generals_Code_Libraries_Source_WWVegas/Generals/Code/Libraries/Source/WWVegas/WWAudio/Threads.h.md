# Generals/Code/Libraries/Source/WWVegas/WWAudio/Threads.h

## Purpose
Manages audio-related threading mechanisms, particularly for delayed object release.

## Responsibilities
- Manages a delayed release thread for safe object cleanup
- Provides thread synchronization primitives
- Handles delayed release of RefCountClass objects
- Manages thread shutdown procedures

## Key Types
- **RefCountClass (Class)**: Reference-counted object base class
- **WWAudioThreadsClass (Class)**: Main class managing audio threads and delayed release
- **_DELAYED_RELEASE_INFO (Struct)**: Contains object pointer, timestamp, and linked list pointer

## Key Functions
### WWAudioThreadsClass::Create_Delayed_Release_Thread
- Purpose: Creates and starts the delayed release thread
- Calls: Not inferable

### WWAudioThreadsClass::End_Delayed_Release_Thread
- Purpose: Stops the delayed release thread with timeout
- Calls: Not inferable

### WWAudioThreadsClass::Add_Delayed_Release_Object
- Purpose: Adds an object to the delayed release queue
- Calls: Not inferable

### WWAudioThreadsClass::Flush_Delayed_Release_Objects
- Purpose: Immediately processes all delayed release objects
- Calls: Not inferable

### WWAudioThreadsClass::Delayed_Release_Thread_Proc
- Purpose: Thread procedure that processes delayed releases
- Calls: Not inferable

## Globals
- **m_hDelayedReleaseThread (HANDLE)**: Handle to the delayed release thread
- **m_hDelayedReleaseEvent (HANDLE)**: Event for thread synchronization
- **m_CriticalSection (CriticalSectionClass)**: Thread synchronization for critical sections
- **m_ReleaseListHead (DELAYED_RELEASE_INFO**)**: Head of the delayed release linked list
- **m_ListMutex
