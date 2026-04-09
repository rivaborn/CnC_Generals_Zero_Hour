# GeneralsMD/Code/GameEngine/Source/GameNetwork/ConnectionManager.cpp

## Purpose
Manages network connections, command relaying, and game synchronization in multiplayer.

## Responsibilities
- Handles network transport and packet routing
- Manages command relaying between players
- Tracks connection states and player slots
- Processes network commands and game messages
- Manages file transfers and chat messages

## Key Types
- **ConnectionManager (Class)**: Main network manager class
- **NetCommandList (Class)**: List of network commands
- **NetPacket (Class)**: Network packet container
- **DisconnectManager (Class)**: Handles player disconnections
- **NetCommandWrapperList (Class)**: Manages command wrappers

## Key Functions
### `doRelay()`
- Purpose: Processes incoming packets and relays commands to appropriate connections
- Calls: `newInstance`, `getCommandList`, `getFirstMessage`, `CommandRequiresAck`, `ackCommand`, `processNetCommand`, `sendRemoteCommand`

### `sendChat()`
- Purpose: Sends chat messages to specified players
- Calls: `newInstance`, `setText`, `setPlayerMask`, `setPlayerID`, `setID`, `GenerateNextCommandID`, `sendLocalCommand`, `processChat`

### `sendFileAnnounce()`
- Purpose: Announces file availability to other players
- Calls: `openFile`, `close`, `newInstance`, `setPlayerID`, `setID`, `GenerateNextCommandID`, `setRealFilename`, `setPlayerMask`, `processFileAnnounce`, `sendLocalCommand`

### `updateLoadProgress()`
- Purpose: Updates load progress for other players
- Calls: `newInstance`, `setPercentage`, `setPlayerID`, `setID`, `GenerateNextCommandID`, `processProgress`, `sendLocalCommand`

## Globals
- **commandsReadyDebugSpewage (Int)**: Debug flag for command processing

## Dependencies
- Key includes: `PreRTS.h`, `Compression.h`, `strtok_r.h`, `Common/AudioEventRTS.h`, `Common/CRCDebug.h`, `Common/Debug.h`, `Common/File.h`, `Common/GameAudio.h`, `Common/LocalFileSystem.h`, `Common/Player.h`, `Common/PlayerList.h`, `Common/RandomValue.h`, `Common/Recorder.h`, `GameClient/Diplomacy.h`, `GameClient/GameText.h`, `GameClient/MessageBox.h`, `GameNetwork/ConnectionManager.h`, `GameNetwork/LANAPICallbacks.h`, `GameNetwork/NAT.h`, `GameNetwork/NetCommandWrapperList.h`, `GameNetwork/NetworkUtil.h`, `GameLogic/GameLogic.h`, `GameLogic/ScriptActions.h`, `GameLogic/ScriptEngine.h`, `GameLogic/VictoryConditions.h`, `GameClient/DisconnectMenu.h`, `GameClient/InGameUI.h`
