# Generals/Code/GameEngine/Source/Common/System/StackDump.cpp

## Purpose
This file provides functionality for generating and handling stack dumps in the Command & Conquer Generals game engine, primarily used for debugging purposes.

## Responsibilities
- Initialize and clean up symbol information for stack trace generation.
- Generate call stacks from different contexts (current thread or provided context).
- Retrieve function details such as name, filename, line number, and address.
- Handle exceptions by dumping detailed information including register states and memory at the point of exception.

## Key Types
- None

## Key Functions
### StackDump
- Purpose: Generates a stack dump using the default handler if no callback is provided.
- Calls:
  - InitSymbolInfo
  - MakeStackTrace

### StackDumpFromContext
- Purpose: Generates a stack dump from a given context (EIP, ESP, EBP).
- Calls:
  - InitSymbolInfo
  - MakeStackTrace

### InitSymbolInfo
- Purpose: Initializes symbol information for stack trace generation.
- Calls:
  - GetModuleHandle
  - GetProcAddress
  - SymSetOptions
  - GetCurrentProcess
  - GetModuleFileName
  - _splitpath
  - sprintf
  - lstrcat
  - SymInitialize
  - SymLoadModule

### UninitSymbolInfo
- Purpose: Cleans up symbol information.
- Calls:
  - SymCleanup

### MakeStackTrace
- Purpose: Walks the stack and calls a callback for each frame.
- Calls:
  - StackWalk
  - WriteStackLine

### GetFunctionDetails
- Purpose: Retrieves function details such as name, filename, line number, and address from a given pointer.
- Calls:
  - SymGetSymFromAddr
  - gsSymGetLineFromAddr

### FillStackAddresses
- Purpose: Fills an array with addresses from the stack.
- Calls:
  - StackWalk

### StackDumpFromAddresses
- Purpose: Generates a stack dump using an array of addresses.
- Calls:
  - WriteStackLine

### WriteStackLine
- Purpose: Writes a formatted line for a given address to the callback and global error dump.
- Calls:
  - GetFunctionDetails

### DumpExceptionInfo
- Purpose: Dumps detailed information about an exception, including stack trace and register states.
- Calls:
  - DEBUG_LOG
  - StackDumpFromContext

## Globals
- gsContext (CONTEXT): Stores context information for stack walking.
- gsInit (Bool): Indicates whether symbol information has been initialized.
- gsSymGetLineFromAddr (function pointer): Pointer to the SymGetLineFromAddr function from dbghelp.dll.
- g_LastErrorDump (AsciiString): Stores the last error dump.

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/StackDump.h"
  - "Common/Debug.h"
- External symbols used:
  - SymGetLineFromAddr
  - GetModuleHandle
  - GetProcAddress
  - SymSetOptions
  - GetCurrentProcess
  - GetModuleFileName
  - _splitpath
  - sprintf
  - lstrcat
  - SymInitialize
  - SymLoadModule
  - SymCleanup
  - StackWalk
  - SymFunctionTableAccess
  - SymGetModuleBase
  - IsBadReadPtr
