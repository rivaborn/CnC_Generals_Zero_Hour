# GeneralsMD/Code/GameEngine/Source/GameNetwork/LANAPICallbacks.cpp

## Purpose
Handles LAN API callbacks for multiplayer game operations in Command & Conquer Generals Zero Hour.

## Responsibilities
- Manages player joins/leaves, game creation/joining, and chat messages
- Handles game options synchronization and player slot management
- Processes map transfers and game start sequences
- Displays UI updates for LAN game state changes
- Manages player acceptance/rejection for game sessions

## Key Types
- **LANAPI (Class)**: Main LAN API interface handling callbacks
- **LANAPIInterface (Class)**: Interface defining callback methods
- **ReturnType (Enum)**: Error/success codes for LAN operations
- **ChatType (Enum)**: Types of chat messages (normal, emote, system)
- **Color (Type)**: Predefined chat message colors

## Key Functions
### OnAccept
- Purpose: Handles player acceptance/rejection responses
- Calls: `m_currentGame->getLANSlot()`, `setAccept()`, `unAccept()`, `RequestGameOptions()`, `lanUpdateSlotList()`

### OnGameStart
- Purpose: Initializes and starts the LAN game
- Calls: `pref.write()`, `NetworkInterface::createNetwork()`, `TheNetwork->init()`, `DoAnyMapTransfers()`, `m_currentGame->startGame()`, `TheMessageStream->appendMessage()`

### OnChat
- Purpose: Displays chat messages in appropriate UI elements
- Calls: `TheLanguageFilter->filterLine()`, `GadgetListBoxAddEntryText()`, `GadgetListBoxSetItemData()`

### OnPlayerJoin
- Purpose: Handles new player joining the game
- Calls: `m_currentGame->resetAccepted()`, `RequestGameOptions()`, `lanUpdateSlotList()`

### OnGameOptions
- Purpose: Processes game option changes from players
- Calls: `ParseGameOptionsString()`, `lanUpdateSlotList()`, `updateGameOptions()`, `RequestGameOptions()`

## Globals
- **TheLAN (LANAPI*)**: Global LAN API instance
- **LANbuttonPushed (Bool)**: Tracks UI button state
- **playerColor (Color)**: White color for player names
- **gameColor (Color)**: White color for game messages
- **gameInProgressColor (Color)**: Gray color for in-progress game text
- **chatNormalColor (Color)**: Cyan color for normal chat
- **chatActionColor (Color)**: Magenta color for emotes/actions
- **chatLocalNormalColor (Color)**: Orange color for local player chat
- **chatLocalActionColor (Color)**: Yellow color for local player emotes
- **chatSystemColor (Color)**: White color for system messages
- **acceptTrueColor (Color)**: Green color for accept confirmations
- **acceptFalseColor (Color)**: Red color for reject notifications

## Dependencies
- Key includes: `PreRTS.h`, `GameEngine.h`, `MessageStream.h`, `MultiplayerSettings.h`, `PlayerTemplate.h`, `GameText.h`, `LanguageFilter.h`, `MapUtil.h`, `MessageBox.h`, `GameLogic.h`, `FileTransfer.h`, `LANAPICallbacks.h`, `NetworkUtil.h`
- External symbols: `TheGameText`, `TheMapCache`, `TheMultiplayerSettings`, `ThePlayerTemplateStore`, `TheShell`, `TheMessageStream`, `TheWritableGlobalData`, `TheGameLogic`, `TheNetwork`, `TheLanguageFilter`, `listboxGames`, `listboxChatWindow`, `listboxPlayers`, `listboxChatWindowScoreScreen`, `listboxChatWindowLanGame`
