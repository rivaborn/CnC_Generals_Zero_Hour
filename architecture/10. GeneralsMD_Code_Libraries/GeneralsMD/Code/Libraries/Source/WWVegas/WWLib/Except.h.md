# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/Except.h

## Purpose
Header file for exception handling and thread management in the SAGE engine.

## Responsibilities
- Declares exception handling functions
- Defines thread registration and management
- Provides stack walking and symbol lookup utilities
- Manages global exception state variables

## Key Types
- EXCEPTION_POINTERS (Class): Windows exception information structure
- CONTEXT (Class): Windows CPU context structure
- tThreadInfoType (Struct): Thread information container
- ThreadInfoType (Struct): Alias for tThreadInfoType

## Key Functions
### Exception_Handler
- Purpose: Handles exceptions in the game
- Calls: Not inferable

### Stack_Walk
- Purpose: Walks the call stack to collect return addresses
- Calls: Not inferable

### Lookup_Symbol
- Purpose: Looks up symbols for addresses in the executable
- Calls: Not inferable

### Register_Thread_ID
- Purpose: Registers a thread with the exception system
- Calls: Not inferable

### Register_Application_Exception_Callback
- Purpose: Registers a callback for application exceptions
- Calls: Not inferable

### Set_Exit_On_Exception
- Purpose: Configures whether to exit on exceptions
- Calls: Not inferable

## Globals
- ExceptionReturnStack (unsigned long): Stack address for exception recovery
- ExceptionReturnAddress (unsigned long): Return address for exception recovery
- ExceptionReturnFrame (unsigned long): Frame pointer for exception recovery

## Dependencies
- win.h: Windows API headers
- HANDLE: Windows handle type
