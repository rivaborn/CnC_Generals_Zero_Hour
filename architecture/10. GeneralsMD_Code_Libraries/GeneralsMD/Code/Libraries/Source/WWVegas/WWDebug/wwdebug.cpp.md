# GeneralsMD/Code/Libraries/Source/WWVegas/WWDebug/wwdebug.cpp

## Purpose
Provides debug utilities for logging, assertions, triggers, and profiling in the SAGE engine.

## Responsibilities
- Manages debug message handlers (installation and invocation)
- Handles system error conversion and retrieval
- Provides assertion failure handling with customizable behavior
- Supports debug triggers and profiling callbacks
- Includes Windows-specific debug output via DBWIN32

## Key Types
- `PrintFunc` (Function pointer): Callback for debug messages
- `AssertPrintFunc` (Function pointer): Callback for assertion failures
- `TriggerFunc` (Function pointer): Callback for debug triggers
- `ProfileFunc` (Function pointer): Callback for profiling start/stop events

## Key Functions
### `Convert_System_Error_To_String`
- Purpose: Converts Windows system error code to human-readable string
- Calls: `FormatMessage`

### `Get_Last_System_Error`
- Purpose: Retrieves the last Windows system error code
- Calls: `GetLastError`

### `WWDebug_Install_Message_Handler`
- Purpose: Installs a callback for debug messages
- Calls: None

### `WWDebug_Install_Assert_Handler`
- Purpose: Installs a callback for assertion failures
- Calls: None

### `WWDebug_Install_Trigger_Handler`
- Purpose: Installs a callback for debug triggers
- Calls: None

### `WWDebug_Install_Profile_Start_Handler`
- Purpose: Installs a callback for profiling start events
- Calls: None

### `WWDebug_Install_Profile_Stop_Handler`
- Purpose: Installs a callback for profiling stop events
- Calls: None

### `WWDebug_Printf`
- Purpose: Logs a debug message
- Calls: `vsprintf`, `_CurMessageHandler`

### `WWDebug_Printf_Warning`
- Purpose: Logs a warning message
- Calls: `vsprintf`, `_CurMessageHandler`

### `WWDebug_Printf_Error`
- Purpose: Logs an error message
- Calls: `vsprintf`, `_CurMessageHandler`

### `WWDebug_Check_Trigger`
- Purpose: Checks if a debug trigger is active
- Calls: `_CurTriggerHandler`

### `WWDebug_Profile_Start`
- Purpose: Notifies profiling start
- Calls: `_CurProfileStartHandler`

### `WWDebug_Profile_Stop`
- Purpose: Notifies profiling stop
- Calls: `_CurProfileStopHandler`

## Globals
- `_CurMessageHandler` (PrintFunc): Current debug message handler
- `_CurAssertHandler` (AssertPrintFunc): Current assertion handler
- `_CurTriggerHandler` (TriggerFunc): Current trigger handler
- `_CurProfileStartHandler` (ProfileFunc): Current profiling start handler
- `_CurProfileStopHandler` (ProfileFunc): Current profiling stop handler

## Dependencies
- `wwdebug.h` (header)
- Windows API (`windows.h`)
- C runtime (`stdlib.h`, `stdarg.h`, `stdio.h`, `string.h`)
- Assert (`assert.h`)
- Signal handling (`signal.h`)
- `except.h` (custom exception handling)
