# GeneralsMD/Code/Libraries/Source/WPAudio/AUD_Assert.cpp

## Purpose
Handles assertion and debug printing functionality for the WPAudio library in debug builds.

## Responsibilities
- Provides debug assertion macros
- Formats and outputs debug messages
- Tracks assertion failures and errors
- Interfaces with Windows debug output

## Key Types
None

## Key Functions
### _assert_printf
- Purpose: Formats a string into the assertion message buffer.
- Calls: vsprintf

### _aud_debug_printf
- Purpose: Formats and outputs a debug message via WindowsDebugPrint.
- Calls: vsprintf, WindowsDebugPrint

### _aud_assert
- Purpose: Handles assertion failures by printing error info and calling _assert.
- Calls: sprintf, WindowsDebugPrint, _assert

## Globals
- DBG_type_struct_is_dead (char*): Default error message for invalid structures
- assert_msg_buf (char[10KB]): Buffer for assertion messages
- err_file (FILE*): File handle for error logging (unused)
- total_errors (int): Counter for total errors (unused)
- _msg_buf (char[20KB]): Buffer for debug messages

## Dependencies
- <string.h>, <stdarg.h>, <assert.h>, <stdio.h>, <time.h>
- wpaudio/altypes.h
- WindowsDebugPrint (external)
