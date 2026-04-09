# Generals/Code/Libraries/Source/WWVegas/WWDebug/wwdebug.cpp

## Purpose
Provides debug utilities including message handling, assertions, triggers, and profiling for the SAGE engine.

## Responsibilities
- Install/manage debug message, assert, trigger, and profile handlers
- Format system errors into strings
- Provide debug output via printf-style functions
- Support Windows debug output via DBWIN32

## Key Types
- PrintFunc (Function): Callback for debug messages
- AssertPrintFunc (Function): Callback for assert failures
- TriggerFunc (Function): Callback for debug triggers
- ProfileFunc (Function): Callback for profiling start/stop

## Key Functions
### Convert_System_Error_To_String
- Purpose: Converts system error code to human-readable string
- Calls: FormatMessage (Windows API)

### WWDebug_Install_Message_Handler
- Purpose: Installs a debug message handler
- Calls: None

### WWDebug_Install_Assert_Handler
- Purpose: Installs an assert handler
- Calls: None

### WWDebug_Install_Trigger_Handler
- Purpose: Installs a trigger handler
- Calls: None

### WWDebug_Install_Profile_Start_Handler
- Purpose: Installs a profile start handler
- Calls: None

### WWDebug_Install_Profile_Stop_Handler
- Purpose: Installs a profile stop handler
- Calls: None

### WWDebug_Check_Trigger
- Purpose: Checks if a debug trigger is active
- Calls: _CurTriggerHandler

### WWDebug_Profile_Start
- Purpose: Starts a profiling section
- Calls: _CurProfileStartHandler

### WWDebug_Profile_Stop
- Purpose: Stops a profiling section
- Calls: _CurProfileStopHandler

## Globals
- _CurMessageHandler (PrintFunc): Current debug message handler
- _CurAssertHandler (AssertPrintFunc): Current assert handler
- _CurTriggerHandler (TriggerFunc): Current trigger handler
- _CurProfileStartHandler (ProfileFunc): Current profile start handler
- _CurProfileStopHandler (ProfileFunc): Current profile stop handler

## Dependencies
- wwdebug.h (header)
- Windows.h (for FormatMessage, GetLastError)
- stdlib.h, stdarg.h, stdio.h, assert.h, string.h (C runtime)
