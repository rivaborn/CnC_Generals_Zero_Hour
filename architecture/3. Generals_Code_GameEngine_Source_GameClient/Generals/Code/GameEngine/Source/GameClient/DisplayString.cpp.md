# Generals/Code/GameEngine/Source/GameClient/DisplayString.cpp

## Purpose
Manages double-byte game string data and rendering text to the screen.

## Responsibilities
- Constructs and manages `DisplayString` objects
- Handles text manipulation (setting, appending, removing characters)
- Notifies observers when text changes
- Manages font references and string storage

## Key Types
- `DisplayString` (Class): Core class for storing and displaying text
- `UnicodeString` (Type): Used for storing text content
- `WideChar` (Type): Represents individual characters

## Key Functions
### `DisplayString::setText`
- Purpose: Sets the text content and notifies observers of changes
- Calls: `notifyTextChanged()`

### `DisplayString::reset`
- Purpose: Clears all data and resets the string to a blank state
- Calls: None

### `DisplayString::removeLastChar`
- Purpose: Removes the last character and notifies observers
- Calls: `notifyTextChanged()`

### `DisplayString::appendChar`
- Purpose: Appends a character and notifies observers
- Calls: `notifyTextChanged()`

## Globals
- None

## Dependencies
- `PreRTS.h`, `Common/Debug.h`, `Common/Language.h`, `GameClient/DisplayString.h`
- `UnicodeString`, `WideChar` (external types)
- `notifyTextChanged()` (external method)
