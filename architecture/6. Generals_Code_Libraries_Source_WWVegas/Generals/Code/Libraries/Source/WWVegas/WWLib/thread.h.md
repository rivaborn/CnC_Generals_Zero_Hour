# Generals/Code/Libraries/Source/WWVegas/WWLib/thread.h

## Purpose
Defines a base class for thread management in the SAGE engine, allowing derived classes to implement custom thread behavior.

## Responsibilities
- Provides thread creation and execution framework
- Manages thread lifecycle (start/stop)
- Handles thread priority and synchronization
- Offers static utility functions for thread control

## Key Types
- ThreadClass (Class): Base class for creating and managing threads

## Key Functions
### ThreadClass::Execute
- Purpose: Starts the thread by executing Thread_Function()
- Calls: Internal_Thread_Function

### ThreadClass::Stop
- Purpose: Stops thread execution with optional timeout
- Calls: Not inferable

### ThreadClass::Sleep_Ms
- Purpose: Puts current thread to sleep for specified milliseconds
- Calls: Not inferable

### ThreadClass::Switch_Thread
- Purpose: Yields CPU to next thread
- Calls: Not inferable

### ThreadClass::Thread_Function
- Purpose: Pure virtual function to be implemented by derived classes
- Calls: Not inferable

### ThreadClass::Internal_Thread_Function
- Purpose: Internal thread entry point that manages the thread lifecycle
- Calls: Thread_Function

## Globals
- None

## Dependencies
- "always.h" (header)
- "osdep.h" (for UNIX builds)
- volatile bool/unsigned long types
- Platform-specific threading APIs (not shown in header)
