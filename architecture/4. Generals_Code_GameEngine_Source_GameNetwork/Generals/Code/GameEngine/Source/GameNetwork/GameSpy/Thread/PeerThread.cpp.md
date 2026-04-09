# Generals/Code/GameEngine/Source/GameNetwork/GameSpy/Thread/PeerThread.cpp

## Purpose
Handles GameSpy peer (chat) communication via a dedicated thread, managing requests/responses through a message queue.

## Responsibilities
- Manages connection to GameSpy chat server
- Processes peer-to-peer messages and room events
- Tracks game hosting information (players, stats, etc.)
- Handles QuickMatch functionality
- Maintains server/staging room lists

## Key Types
- **PeerThreadClass (Class)**: Main thread class handling GameSpy communication
- **GameSpyPeerMessageQueue (Class)**: Message queue interface for thread communication
- **CallbackType (Enum)**: Types of GameSpy callbacks (connect, error, messages, etc.)
- **RoomType (Enum)**: Room types (group/staging)
- **QMStatus (Enum)**: QuickMatch status states

## Key Functions
### connectCallback
- Purpose: Handles connection success/failure from GameSpy server
- Calls: `markAsDisconnected`, queue operations

### listingGamesCallback
- Purpose: Processes game listing updates from server
- Calls: `findServer`, `removeServerFromMap`, queue operations

### playerJoinedCallback
- Purpose: Handles player join events in rooms
- Calls: `getPlayerInfo`, queue operations

### roomKeyChangedCallback
- Purpose: Tracks player statistics changes
- Calls: `trackStatsForPlayer`, `getPlayerInfo`, queue operations

### doQuickMatch
- Purpose: Initiates QuickMatch game finding
- Calls: Various GameSpy API functions

## Globals
- **TheGameSpyPeerMessageQueue (GameSpyPeerMessageQueue**)**: Global message queue instance
- **isThreadHosting (int)**: Tracks if thread is hosting a game
- **qr2Sock (SOCKET)**: Socket for QuickMatch communication
- **localIP (string)**: Local IP address for hosting

## Dependencies
- GameSpy Peer API headers
- Threading utilities (MutexClass, ThreadClass)
- Common utilities (Registry, Version, etc.)
- Networking components (IPEnumeration)
- STL containers (queue, map)
