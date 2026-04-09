# GeneralsMD/Code/GameEngine/Source/GameNetwork/GameSpy/Thread/PeerThread.cpp

## Purpose
Handles GameSpy peer (chat) communication via a dedicated thread, managing requests/responses through a message queue.

## Responsibilities
- Manages connection/disconnection to GameSpy servers
- Processes peer-to-peer messages and room events
- Tracks game hosting information (players, stats, etc.)
- Handles QuickMatch functionality and player statistics
- Bridges between GameSpy API and internal game systems

## Key Types
- **PeerThreadClass (Class)**: Main thread class handling GameSpy peer operations
- **GameSpyPeerMessageQueue (Class)**: Message queue for request/response communication
- **CallbackType (Enum)**: Types of GameSpy callbacks (connect, error, messages, etc.)
- **RoomType (Enum)**: Room types (group/staging)
- **QMStatus (Enum)**: QuickMatch status states

## Key Functions
### connectCallback
- Purpose: Handles GameSpy connection success/failure
- Calls: `markAsDisconnected`, queue operations

### listingGamesCallback
- Purpose: Processes staging room game listings (add/update/remove)
- Calls: `findServer`, `removeServerFromMap`, queue operations

### playerJoinedCallback
- Purpose: Handles player joining a room
- Calls: `getPlayerInfo`, queue operations

### roomKeyChangedCallback
- Purpose: Processes room key/value changes
- Calls: `trackStatsForPlayer`, `getPlayerInfo`, queue operations

### doQuickMatch
- Purpose: Initiates QuickMatch game finding
- Calls: Various GameSpy API functions

## Globals
- **isThreadHosting (int)**: Tracks if thread is hosting a game
- **qr2Sock (SOCKET)**: QuickMatch socket handle
- **TheGameSpyPeerMessageQueue (GameSpyPeerMessageQueueInterface**)**: Global message queue instance
- **localIP (string)**: Local IP address
- **matchbotProfileID (int)**: Profile ID for matchbot

## Dependencies
- GameSpy peer API headers
- Threading utilities (`thread.h`, `mutex.h`)
- Game engine utilities (`PreRTS.h`, `Common/` headers)
- Networking components (`IPEnumeration.h`)
- Logging utilities (`MiniLog.h`)
