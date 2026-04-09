# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/thread.h

## Purpose
Defines a cross-platform thread abstraction class for the SAGE engine.

## Responsibilities
- Provides thread creation, execution, and management
- Handles thread priority, stopping, and sleeping
- Supports exception handling in threads
- Tracks thread state and identity

## Key Types
- ThreadClass (Class): Base class for creating game threads
- ExceptionHandlerType (Function pointer): Callback for thread exceptions
- _EXCEPTION_POINTERS (Struct): Windows exception info (external)

## Key Functions
### ThreadClass::Execute
- Purpose: Starts the thread's execution
- Calls: Internal_Thread_Function

### ThreadClass::Stop
- Purpose: Stops thread execution with timeout
- Calls: None visible

### ThreadClass::Sleep_Ms
- Purpose: Pauses current thread for milliseconds
- Calls: None visible

### ThreadClass::Switch_Thread
- Purpose: Yields CPU to next thread
- Calls: None visible

### ThreadClass::Thread_Function
- Purpose: Pure virtual function for thread logic
- Calls: None visible

## Globals
- None

## Dependencies
- "always.h", "vector.h" (internal headers)
- _EXCEPTION_POINTERS (Windows struct)
- Platform-specific headers via "osdep.h"
