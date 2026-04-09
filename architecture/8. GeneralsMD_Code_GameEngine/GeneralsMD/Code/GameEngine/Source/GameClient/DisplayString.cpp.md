# GeneralsMD/Code/GameEngine/Source/GameClient/DisplayString.cpp

## Purpose
Manages double-byte game string data and rendering text to the screen.

## Responsibilities
- Stores and manipulates Unicode text strings
- Manages font associations for text rendering
- Handles text change notifications
- Provides basic string operations (append, remove)

## Key Types
- **DisplayString (Class)**: Holds text and font data for display
- **UnicodeString (Type)**: Used for storing double-byte text

## Key Functions
### DisplayString::setText
- Purpose: Sets the text content and notifies of changes
- Calls: `notifyTextChanged()`

### DisplayString::reset
- Purpose: Clears all data and resets the instance
- Calls: None

### DisplayString::removeLastChar
- Purpose: Removes the last character and notifies of changes
- Calls: `notifyTextChanged()`

### DisplayString::appendChar
- Purpose: Appends a character and notifies of changes
- Calls: `notifyTextChanged()`

## Globals
- None

## Dependencies
- `Common/Debug.h`
- `Common/Language.h`
- `GameClient/DisplayString.h`
- `UnicodeString` (from Language.h)
- `WideChar` (from Language.h)
