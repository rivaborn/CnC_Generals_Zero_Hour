# Generals/Code/Libraries/Source/WWVegas/WWDebug/wwdebug.h

## Purpose
Header file defining debug utilities and macros for the SAGE engine.

## Responsibilities
- Declares debug message, assertion, trigger, and profiling interfaces
- Provides conditional compilation macros for debug/release builds
- Defines system error conversion utilities

## Key Types
- DebugType (Enum): debug message severity levels (info, warning, error, user)
- PrintFunc (Function pointer): callback for debug messages
- AssertPrintFunc (Function pointer): callback for assertion failures
- TriggerFunc (Function pointer): callback for debug triggers
- ProfileFunc (Function pointer): callback for profiling events

## Key Functions
### Convert_System_Error_To_String
- Purpose: Converts system error codes to human-readable strings
- Calls: None

### Get_Last_System_Error
- Purpose: Retrieves the last system error code
- Calls: None

### WWDebug_Install_Message_Handler
- Purpose: Installs a custom debug message handler
- Calls: None

### WWDebug_Install_Assert_Handler
- Purpose: Installs a custom assertion handler
- Calls: None

### WWDebug_Install_Trigger_Handler
- Purpose: Installs a custom debug trigger handler
- Calls: None

### WWDebug_Install_Profile_Start_Handler
- Purpose: Installs a custom profiling start handler
- Calls: None

### WWDebug_Install_Profile_Stop_Handler
- Purpose: Installs a custom profiling stop handler
- Calls: None

## Globals
- None

## Dependencies
- "..\..\..\..\gameengine\include\common\debug.h"
- Windows-specific headers (for _asm int 0x03)
- Standard C runtime (for variadic functions)
