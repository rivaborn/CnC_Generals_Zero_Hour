# Generals/Code/Libraries/Source/WWVegas/WWLib/thread.cpp

## Purpose
Implements a cross-platform thread wrapper class for the SAGE engine, primarily targeting Windows.

## Responsibilities
- Manages thread creation, execution, and termination
- Provides thread priority control
- Offers basic thread synchronization utilities
- Handles platform-specific differences (Windows/Unix)
- Exposes thread ID retrieval

## Key Types
- ThreadClass (Class): Thread management wrapper
- None (other types)

## Key Functions
### ThreadClass::Execute
- Purpose: Starts the thread execution
- Calls: _beginthread, SetThreadPriority

### ThreadClass::Stop
- Purpose: Stops the thread execution
- Calls: TerminateThread, Sleep

### ThreadClass::Switch_Thread
- Purpose: Yields thread execution
- Calls: WaitForSingleObject

### ThreadClass::_Get_Current_Thread_ID
- Purpose: Retrieves the current thread's ID
- Calls: GetCurrentThreadId

## Globals
- test_event (HANDLE): Event object for thread switching

## Dependencies
- thread.h (header)
- wwdebug.h (assertions)
- process.h (_beginthread)
- windows.h (thread APIs)
- mmsystem.h (timeGetTime)
