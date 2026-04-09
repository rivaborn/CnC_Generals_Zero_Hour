# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/InGameChat.cpp

## Purpose
Handles GUI callbacks for in-game chat functionality, including display, input, and message sending.

## Responsibilities
- Manages in-game chat window creation/destruction
- Handles chat input and message transmission
- Processes slash commands (e.g., `/host`)
- Controls chat visibility and focus management
- Filters and routes chat messages to appropriate players

## Key Types
- `InGameChatType` (Enum): Defines chat scope (everyone/allies/players)
- `GameWindow` (Class): Base window class for UI elements
- `UnicodeString` (Class): Unicode text handling

## Key Functions
### `ShowInGameChat`
- Purpose: Creates/displays the chat window and text entry field
- Calls: `TheWindowManager->winCreateFromScript`, `GadgetTextEntrySetText`, `SetInGameChatType`

### `ToggleInGameChat`
- Purpose: Toggles chat visibility and sends messages when hidden
- Calls: `GadgetTextEntryGetText`, `TheLanguageFilter->filterLine`, `TheNetwork->sendChat`

### `handleInGameSlashCommands`
- Purpose: Processes slash commands (e.g., `/host`)
- Calls: `TheInGameUI->message`, `getQR2HostingStatus`

### `InGameChatSystem`
- Purpose: Handles window system messages (focus, input, button clicks)
- Calls: `ToggleInGameChat`, `GadgetTextEntrySetText`

## Globals
- `chatWindow` (`GameWindow*`): Main chat window
- `chatTextEntry` (`GameWindow*`): Text input field
- `chatTypeStaticText` (`GameWindow*`): Displays current chat type
- `s_savedChat` (`UnicodeString`): Preserves chat text when hidden
- `inGameChatType` (`InGameChatType`): Current chat scope
- `isThreadHosting` (`int`): External hosting status flag

## Dependencies
- `GameClient/Gadget.h`, `GameClient/GadgetTextEntry.h`
- `GameNetwork/NetworkInterface.h`, `GameClient/LanguageFilter.h`
- `TheWindowManager`, `TheGameLogic`, `ThePlayerList`, `TheNetwork`
