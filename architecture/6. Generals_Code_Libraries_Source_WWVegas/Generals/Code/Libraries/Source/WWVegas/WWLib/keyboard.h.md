# Generals/Code/Libraries/Source/WWVegas/WWLib/keyboard.h

## Purpose
Header file defining keyboard input handling classes and enums for the SAGE engine.

## Responsibilities
- Define keyboard input classes (`WWKeyboardClass`, `KeyboardClass`)
- Provide key code enums (`KeyASCIIType`, `KeyNumType`)
- Handle keyboard state tracking and message processing
- Support mouse input through keyboard class

## Key Types
- `WWKey_Type` (Enum): Bit flags for keyboard modifiers (shift, ctrl, alt, etc.)
- `WWKeyboardClass` (Class): Core keyboard input handling class
- `KeyASCIIType` (Enum): ASCII character key codes
- `KeyNumType` (Enum): Numeric/functional key codes
- `KeyboardClass` (Class): Wrapper class for game-specific keyboard interface

## Key Functions
### `WWKeyboardClass::Message_Handler`
- Purpose: Processes Windows messages for keyboard input
- Calls: `Put_Key_Message`, `Put_Mouse_Message`, `Fill_Buffer_From_System`

### `WWKeyboardClass::To_ASCII`
- Purpose: Converts key codes to ASCII characters
- Calls: None

### `KeyboardClass::Get`
- Purpose: Retrieves next key from input buffer
- Calls: `WWKeyboardClass::Get`

## Globals
- `VK_*` (Constants): Virtual key code definitions
- `KA_*` (Constants): ASCII key type mappings
- `KN_*` (Constants): Numeric key type mappings

## Dependencies
- `_xmouse.h`: Mouse input handling
- `win.h`: Windows API headers
- `bool.h`: Boolean type definition
