# Generals/Code/GameEngine/Source/GameClient/Input/Keyboard.cpp

## Purpose
Handles keyboard input processing, key state tracking, and message generation for the game engine.

## Responsibilities
- Manages keyboard state and key translations
- Generates game messages from keyboard input
- Handles key repeat logic and modifier states
- Initializes language-specific key mappings
- Provides access to key status and state data

## Key Types
- Keyboard (Class): Main keyboard input handler
- KeyboardIO (Struct): Represents individual key input data
- KeyStatus (Struct): Tracks key state and sequence data
- KeyNames (Struct): Stores character mappings for keys

## Key Functions
### createStreamMessages
- Purpose: Creates game messages from keyboard input state
- Calls: TheMessageStream->appendMessage

### updateKeys
- Purpose: Updates all key state data from input device
- Calls: getKey, resetKeys, translateKey, checkKeyRepeat

### checkKeyRepeat
- Purpose: Checks for key repeat sequences and generates repeat events
- Calls: None

### initKeyNames
- Purpose: Initializes language-specific key character mappings
- Calls: None

### translateKey
- Purpose: Translates key codes to Unicode characters with modifier support
- Calls: getKeyStatusData, getKeyStateBit, setKeyStatusData

## Globals
- TheKeyboard (Keyboard*): Global keyboard input handler instance

## Dependencies
- Common/Language.h
- Common/GameEngine.h
- Common/MessageStream.h
- GameClient/Keyboard.h
- GameClient/KeyDefs.h
- PreRTS.h
