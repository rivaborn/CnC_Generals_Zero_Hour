# GeneralsMD/Code/Libraries/Source/WWVegas/WWDebug/wwdebug.h

## Purpose
Header file defining debug utilities and macros for the SAGE engine.

## Responsibilities
- Declares debug message, assertion, trigger, and profiling interfaces
- Defines conditional compilation macros for debug/release builds
- Provides system error conversion utilities

## Key Types
- DebugType (Enum): debug message severity levels
- PrintFunc (Function pointer): debug message handler
- AssertPrintFunc (Function pointer): assertion handler
- TriggerFunc (Function pointer): debug trigger checker
- ProfileFunc (Function pointer): profiling timer handler

## Key Functions
### WWDebug_Printf
- Purpose: Outputs formatted debug message
- Calls: None

### WWDebug_Printf_Warning
- Purpose: Outputs formatted warning message
- Calls: None

### WWDebug_Printf_Error
- Purpose: Outputs formatted error message
- Calls: None

### Convert_System_Error_To_String
- Purpose: Converts system error code to string
- Calls: None

### Get_Last_System_Error
- Purpose: Retrieves last system error code
- Calls: None

## Globals
- None

## Dependencies
- "..\..\..\..\gameengine\include\common\debug.h"
- Windows system error codes
- C runtime printf formatting
