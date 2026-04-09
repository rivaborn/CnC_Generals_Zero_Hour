# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/keyboard.h

## Purpose
Header file defining keyboard input handling classes and enums for the SAGE engine.

## Responsibilities
- Declares keyboard input classes (`WWKeyboardClass`, `KeyboardClass`)
- Defines key enums (`KeyASCIIType`, `KeyNumType`, `WWKey_Type`)
- Provides virtual key code mappings
- Exposes keyboard state management functions

## Key Types
- `WWKey_Type` (Enum): Bit flags for keyboard modifiers (shift/ctrl/alt)
- `WWKeyboardClass` (Class): Core keyboard input handling implementation
- `KeyASCIIType` (Enum): ASCII character key mappings
- `KeyNumType` (Enum): Numeric/virtual key mappings
- `KeyboardClass` (Class): Game-facing keyboard interface wrapper

## Key Functions
### `WWKeyboardClass::Message_Handler`
- Purpose: Windows message loop handler for keyboard input
- Calls: `Put_Key_Message`, `Put_Mouse_Message`, `Fill_Buffer_From_System`

### `WWKeyboardClass::Put_Key_Message`
- Purpose: Adds key press/release events to input buffer
- Calls: `Put_Element`

### `WWKeyboardClass::Put_Mouse_Message`
- Purpose: Handles mouse input events
- Calls: `Put_Element`

## Globals
- `VK_*` (Macros): Virtual key code definitions
- `KA_*` (Enum values): ASCII key mappings
- `KN_*` (Enum values): Numeric key mappings

## Dependencies
- `_xmouse.h`, `win.h`, `bool.h`
- Windows API types (`HWND`, `UINT`, `LONG`)
- External mouse coordinate functions (`Get_Mouse_X/Y`)
