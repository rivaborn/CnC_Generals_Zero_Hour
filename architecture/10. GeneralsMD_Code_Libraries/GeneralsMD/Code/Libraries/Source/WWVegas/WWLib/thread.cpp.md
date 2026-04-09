# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/thread.cpp

## Purpose
Implements a cross-platform thread wrapper class for Windows, providing thread creation, management, and synchronization.

## Responsibilities
- Manages thread lifecycle (start/stop)
- Handles thread priorities and exceptions
- Provides thread synchronization primitives
- Tracks thread IDs and names for debugging

## Key Types
- ThreadClass (Class): wrapper for OS threads with priority/exception handling
- ExceptionHandlerType (Type): function pointer for exception handling

## Key Functions
### ThreadClass::Execute
- Purpose: Starts the thread execution
- Calls: _beginthread, SetThreadPriority, WWDEBUG_SAY

### ThreadClass::Stop
- Purpose: Stops the thread, with optional timeout
- Calls: TerminateThread, Sleep

### ThreadClass::Switch_Thread
- Purpose: Yields CPU time to other threads
- Calls: WaitForSingleObject

### ThreadClass::_Get_Current_Thread_ID
- Purpose: Returns the current thread's ID
- Calls: GetCurrentThreadId

## Globals
- test_event (HANDLE): synchronization event for thread switching

## Dependencies
- thread.h, except.h, wwdebug.h, systimer.h
- Windows API: _beginthread, SetThreadPriority, TerminateThread, Sleep, GetCurrentThreadId, WaitForSingleObject, CreateEvent
