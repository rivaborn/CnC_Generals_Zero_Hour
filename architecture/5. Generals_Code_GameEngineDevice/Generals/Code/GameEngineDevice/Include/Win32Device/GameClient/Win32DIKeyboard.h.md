# Generals/Code/GameEngineDevice/Include/Win32Device/GameClient/Win32DIKeyboard.h

## Purpose
Header file defining the DirectInputKeyboard class for Windows keyboard input using DirectInput.

## Responsibilities
- Declares DirectInputKeyboard class inheriting from Keyboard
- Defines methods for keyboard initialization, updates, and key state retrieval
- Manages DirectInput device creation and cleanup

## Key Types
- DirectInputKeyboard (Class): Windows DirectInput keyboard interface implementation

## Key Functions
### DirectInputKeyboard::init
- Purpose: Initialize the keyboard device
- Calls: openKeyboard

### DirectInputKeyboard::update
- Purpose: Update keyboard state
- Calls: Not inferable

### DirectInputKeyboard::getKey
- Purpose: Retrieve state of a single key
- Calls: Not inferable

### DirectInputKeyboard::openKeyboard
- Purpose: Create DirectInput keyboard device
- Calls: Not inferable

### DirectInputKeyboard::closeKeyboard
- Purpose: Release DirectInput keyboard device
- Calls: Not inferable

## Globals
- None

## Dependencies
- `<dinput.h>` for DirectInput API
- `GameClient/Keyboard.h` for base Keyboard class
- `LPDIRECTINPUT8`, `LPDIRECTINPUTDEVICE8` from DirectInput
