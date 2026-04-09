# GeneralsMD/Code/GameEngine/Include/Common/OSDisplay.h

## Purpose
Header defining OS display utilities for warning boxes and dialog controls.

## Responsibilities
- Declares button types for OS dialogs
- Defines flags for dialog behavior and icons
- Exposes the `OSDisplayWarningBox` function

## Key Types
- AsciiString (Class): String type used for dialog text
- OSDisplayButtonType (Enum): Dialog button types (OK, CANCEL, ERROR)
- OSDisplayOtherFlags (Enum): Dialog flags (modality, icons)

## Key Functions
### OSDisplayWarningBox
- Purpose: Displays a localized warning dialog with specified text and buttons
- Calls: Not inferable (implementation not shown)

## Globals
None

## Dependencies
- "Lib/Basetype.h" (for `UnsignedInt`)
- `AsciiString` class (forward-declared)
