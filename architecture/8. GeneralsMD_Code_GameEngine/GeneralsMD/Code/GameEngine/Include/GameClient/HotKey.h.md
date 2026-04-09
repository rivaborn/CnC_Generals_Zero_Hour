# GeneralsMD/Code/GameEngine/Include/GameClient/HotKey.h

## Purpose
Defines the hotkey system for the game, including hotkey management and translation.

## Responsibilities
- Manage hotkey registration and execution
- Translate game messages into hotkey actions
- Provide search functionality for hotkeys
- Initialize and reset the hotkey subsystem

## Key Types
- **HotKeyTranslator (Class)**: Translates game messages for hotkey handling
- **HotKey (Class)**: Represents a single hotkey binding to a window
- **HotKeyManager (Class)**: Manages the collection of hotkeys and their execution
- **HotKeyMap (Class)**: Internal map structure for storing hotkey bindings

## Key Functions
### HotKeyTranslator::translateGameMessage
- Purpose: Translates game messages into hotkey actions
- Calls: Not inferable

### HotKeyManager::init
- Purpose: Initializes the hotkey system
- Calls: Not inferable

### HotKeyManager::reset
- Purpose: Resets the hotkey system state
- Calls: Not inferable

### HotKeyManager::addHotKey
- Purpose: Registers a new hotkey binding
- Calls: Not inferable

### HotKeyManager::executeHotKey
- Purpose: Executes a hotkey by its string identifier
- Calls: Not inferable

### HotKeyManager::searchHotKey
- Purpose: Searches for a hotkey by its label (two overloads)
- Calls: Not inferable

## Globals
- **TheHotKeyManager (HotKeyManager*)**: Global instance of the hotkey manager

## Dependencies
- `Common/SubsystemInterface.h`
- `Common/MessageStream.h`
- `AsciiString` (forward reference)
- `GameWindow` (forward reference)
- `GameMessageTranslator` (base class
