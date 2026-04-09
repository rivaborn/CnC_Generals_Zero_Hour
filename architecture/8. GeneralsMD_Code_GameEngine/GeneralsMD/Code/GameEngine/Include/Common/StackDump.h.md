# GeneralsMD/Code/GameEngine/Include/Common/StackDump.h

## Purpose
Header for stack dumping utilities used for debugging and crash reporting in the SAGE engine.

## Responsibilities
- Declares stack trace capture functions
- Provides exception info dumping
- Manages global error dump storage
- Conditionally compiles debug-only functionality

## Key Types
- None

## Key Functions
### StackDump
- Purpose: Dumps current stack trace using a callback or OutputDebugString
- Calls: callback (if provided)

### StackDumpFromContext
- Purpose: Dumps stack trace from given EIP/ESP/EBP context
- Calls: callback (if provided)

### FillStackAddresses
- Purpose: Retrieves stack addresses into provided array
- Calls: None

### StackDumpFromAddresses
- Purpose: Dumps stack trace from pre-filled address array
- Calls: callback (if provided)

### GetFunctionDetails
- Purpose: Retrieves function name, file, line number for a given address
- Calls: None

### DumpExceptionInfo
- Purpose: Dumps exception info and stack trace for crash reporting
- Calls: StackDumpFromContext, callback

## Globals
- g_LastErrorDump (AsciiString): Stores the last generated error dump

## Dependencies
- AsciiString (external type)
- EXCEPTION_POINTERS (Windows SDK)
- OutputDebugString (Windows API)
