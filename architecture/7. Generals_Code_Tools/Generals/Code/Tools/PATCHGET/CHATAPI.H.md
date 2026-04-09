# Generals/Code/Tools/PATCHGET/CHATAPI.H

## Purpose
Header file for chat functionality in the PATCHGET tool, likely providing an API for in-game chat.

## Responsibilities
- Declares chat initialization/shutdown functions
- Provides string fetching for chat messages
- Defines utility macros for array size calculation
- Includes necessary Windows COM and control headers

## Key Types
- None

## Key Functions
### Startup_Chat
- Purpose: Initialize chat system
- Calls: Not inferable

### Shutdown_Chat
- Purpose: Clean up chat system resources
- Calls: Not inferable

### Update_If_Required
- Purpose: Update chat state if needed
- Calls: Not inferable

### Fetch_String
- Purpose: Retrieve localized chat string by ID
- Calls: Not inferable

## Globals
- None

## Dependencies
- `cominit.h` (custom COM initialization)
- Windows headers: `<windows.h>`, `<commctrl.h>`, `<winerror.h>`
- COM/OLE headers: `<ocidl.h>`, `<olectl.h>`
- Standard C: `<stdio.h>`
