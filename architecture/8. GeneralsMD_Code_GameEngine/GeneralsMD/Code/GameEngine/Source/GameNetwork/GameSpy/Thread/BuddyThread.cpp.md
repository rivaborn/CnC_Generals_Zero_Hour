# GeneralsMD/Code/GameEngine/Source/GameNetwork/GameSpy/Thread/BuddyThread.cpp

## Purpose
Manages GameSpy buddy list functionality via a dedicated thread, handling login, messaging, and presence updates.

## Responsibilities
- Manages GameSpy buddy connection lifecycle (login/logout)
- Processes buddy requests/messages/status updates
- Queues responses for UI consumption
- Handles error conditions and disconnections

## Key Types
- **GameSpyBuddyMessageQueue (Class)**: Thread-safe message queue for buddy operations
- **BuddyThreadClass (Class)**: Main thread class handling GameSpy communication
- **CallbackType (Enum)**: Types of GameSpy callbacks (connect, error, message, etc.)

## Key Functions
### callbackWrapper
- Purpose: Routes GameSpy callbacks to appropriate thread methods
- Calls: `connectCallback`, `errorCallback`, `messageCallback`, `requestCallback`, `statusCallback`

### getNickForMessage
- Purpose: Retrieves sender nickname for incoming messages
- Calls: `gpGetInfo`

### getInfoResponseForRequest
- Purpose: Populates response with requester profile info
- Calls: `gpGetInfo`

### getInfoResponseForStatus
- Purpose: Populates response with status changer profile info
- Calls: `gpGetInfo`

## Globals
- **TheGameSpyBuddyMessageQueue (GameSpyBuddyMessageQueueInterface*)**: Singleton message queue instance

## Dependencies
- GameSpy SDK headers (`GPConnection`, `GPErrorArg`, etc.)
- Threading utilities (`MutexClass`, `ThreadClass`)
- Other GameSpy queues (`TheGameSpyPeerMessageQueue`)
- String conversion utilities (`WideCharStringToMultiByte`, `MultiByteToWideCharSingleLine`)
