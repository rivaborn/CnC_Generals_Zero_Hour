# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/InGameChat.cpp

## Purpose
Manages in-game chat UI functionality, including display, input handling, and message transmission.

## Responsibilities
- Show/hide chat window and text entry
- Handle chat input and slash commands
- Manage chat message transmission based on player relationships
- Reset chat state when needed
- Track chat type (everyone/allies/players)

## Key Types
- `InGameChatType` (Enum): Chat target scope (everyone/allies/players)
- `GameWindow` (Class): UI window handle
- `UnicodeString` (Class): Unicode text container

## Key Functions
### `ShowInGameChat`
- Purpose: Creates or displays the chat window with text entry.
- Calls: `winCreateFromScript`, `winGetWindowFromId`, `GadgetTextEntrySetText`, `winSetFocus`, `SetInGameChatType`

### `ToggleInGameChat`
- Purpose: Toggles chat visibility and sends messages when hidden.
- Calls: `GadgetTextEntryGetText`, `handleInGameSlashCommands`, `TheLanguageFilter->filterLine`, `TheNetwork->sendChat`, `HideInGameChat`

### `handleInGameSlashCommands`
- Purpose: Processes slash commands (e.g., `/host`).
- Calls: `getQR2HostingStatus` (external)

### `InGameChatSystem`
- Purpose: Handles window system messages (focus, input, button clicks).
- Calls: `ToggleInGameChat`, `GadgetTextEntrySetText`

## Globals
- `chatWindow` (`GameWindow*`): Main chat window handle
- `chatTextEntry` (`GameWindow*`): Text entry gadget handle
- `chatTypeStaticText` (`GameWindow*`): Chat type display handle
- `s_savedChat` (`UnicodeString`): Stores chat text when hidden
- `inGameChatType` (`InGameChatType`): Current chat target scope
- `isThreadHosting` (`int`): External hosting status flag

## Dependencies
- `GameWindow`, `GadgetTextEntry`, `GadgetStaticText` (UI components)
- `TheWindowManager`, `TheNameKeyGenerator` (window management)
- `ThePlayerList`, `TheGameText`, `TheLanguageFilter`, `TheNetwork` (game systems)
- `getQR2HostingStatus()` (external C function)
