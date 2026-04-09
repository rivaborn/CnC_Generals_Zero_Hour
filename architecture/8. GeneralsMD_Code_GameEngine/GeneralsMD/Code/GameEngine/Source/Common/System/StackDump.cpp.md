# GeneralsMD/Code/GameEngine/Source/Common/System/StackDump.cpp

## Purpose
Handles stack tracing and exception dumping for debugging purposes in debug/internal builds.

## Responsibilities
- Captures and formats call stack information
- Retrieves symbol and line information from addresses
- Generates exception reports with register dumps
- Provides stack trace utilities for crash analysis

## Key Types
- `CONTEXT` (struct): Windows context structure for thread state
- `STACKFRAME` (struct): Stack frame information for walking
- `IMAGEHLP_LINE` (struct): Line information from symbols

## Key Functions
### `StackDump`
- Purpose: Generates a stack trace and outputs it via callback
- Calls: `InitSymbolInfo`, `MakeStackTrace`

### `StackDumpFromContext`
- Purpose: Generates stack trace from exception context
- Calls: `InitSymbolInfo`, `MakeStackTrace`

### `GetFunctionDetails`
- Purpose: Retrieves symbol information for a given address
- Calls: `SymGetSymFromAddr`, `gsSymGetLineFromAddr`

### `DumpExceptionInfo`
- Purpose: Generates detailed exception report including registers and stack
- Calls: `StackDumpFromContext`, `DEBUG_LOG`

## Globals
- `gsContext` (CONTEXT): Stores current thread context
- `gsInit` (Bool): Tracks symbol initialization state
- `gsSymGetLineFromAddr` (function pointer): Symbol helper function
- `g_LastErrorDump` (AsciiString): Accumulates error dump text

## Dependencies
- `Dbghelp.lib` (linker)
- Windows API: `SymInitialize`, `SymCleanup`, `StackWalk`, etc.
- Internal: `DEBUG_LOG`, `AsciiString`
