# Generals/Code/GameEngine/Source/GameClient/MessageStream/HotKey.cpp

## Purpose
Manages hotkey functionality for the game, including registration, execution, and translation of keyboard input into game actions.

## Responsibilities
- Registers and maps hotkeys to game windows
- Executes hotkey actions when triggered
- Translates raw key events into game messages
- Handles hotkey sound feedback

## Key Types
- **HotKey (struct)**: Stores a hotkey mapping (key + target window)
- **HotKeyManager (class)**: Manages the hotkey registry and execution
- **HotKeyTranslator (class)**: Translates key events into hotkey actions

## Key Functions
### `HotKeyTranslator::translateGameMessage`
- Purpose: Converts raw key events into hotkey actions
- Calls: `TheHotKeyManager->executeHotKey`, `TheKeyboard->getPrintableKey`

### `HotKeyManager::executeHotKey`
- Purpose: Executes a registered hotkey action
- Calls: `TheWindowManager->winSendSystemMsg`, `TheAudio->addAudioEvent`

### `HotKeyManager::addHotKey`
- Purpose: Registers a new hotkey mapping
- Calls: None (directly)

### `HotKeyManager::searchHotKey`
- Purpose: Extracts the hotkey character from a labeled string
- Calls: `TheGameText->fetch`

## Globals
- **TheHotKeyManager (HotKeyManager*)**: Singleton instance of the hotkey manager

## Dependencies
- `GameClient/HotKey.h`, `GameClient/KeyDefs.h`, `GameClient/MetaEvent.h`
- `GameClient/GameWindow.h`, `GameClient/GameWindowManager.h`
- `GameClient/keyboard.h`, `GameClient/GameText.h`
- `Common/AudioEventRTS.h`
