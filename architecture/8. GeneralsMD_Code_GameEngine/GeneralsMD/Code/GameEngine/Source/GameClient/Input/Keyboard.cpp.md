# GeneralsMD/Code/GameEngine/Source/GameClient/Input/Keyboard.cpp

## Purpose
Handles keyboard input processing, key state tracking, and translation to Unicode characters.

## Responsibilities
- Manages keyboard state (key presses, releases, modifiers)
- Translates key codes to Unicode characters based on language/keyboard layout
- Generates game messages for key events
- Handles key repeat logic and focus management

## Key Types
- Keyboard (Class): Main keyboard input handler
- KeyboardIO (Struct): Represents individual key state
- KeyName (Struct): Stores key character mappings for different shift states

## Key Functions
### createStreamMessages
- Purpose: Creates game messages for key events and adds them to the message stream
- Calls: TheMessageStream->appendMessage

### updateKeys
- Purpose: Updates internal key state data from raw input
- Calls: getKey, resetKeys, translateKey, checkKeyRepeat

### checkKeyRepeat
- Purpose: Checks for and handles key repeat sequences
- Calls: None

### translateKey
- Purpose: Translates key codes to Unicode characters considering shift states
- Calls: getKeyStatusData, getKeyStateBit, setKeyStatusData, isShift, getCapsState

## Globals
- TheKeyboard (Keyboard*): Global keyboard instance pointer

## Dependencies
- PreRTS.h, Language.h, GameEngine.h, MessageStream.h, Keyboard.h, KeyDefs.h
- GameMessage, KeyboardIO, KeyName, KEY_STATE_*, KEY_* constants
