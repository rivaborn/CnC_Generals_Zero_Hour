# Generals/Code/GameEngine/Source/GameNetwork/GameSpy/Thread/BuddyThread.cpp

## Purpose
Manages GameSpy buddy list functionality via a dedicated thread, handling login, messaging, and presence updates.

## Responsibilities
- Manages GameSpy buddy connection lifecycle (login/logout)
- Processes buddy requests/messages/status updates
- Queues responses for UI consumption
- Handles error conditions and disconnections

## Key Types
- **GameSpyBuddyMessageQueue (Class)**: Thread-safe message queue for buddy operations
- **BuddyThreadClass (Class)**: Main thread class handling GameSpy buddy protocol
- **CallbackType (Enum)**: Callback types for GameSpy events

## Key Functions
### callbackWrapper
- Purpose: Routes GameSpy callbacks to appropriate thread methods
- Calls: thread->connectCallback, thread->errorCallback, thread->messageCallback, thread->requestCallback, thread->statusCallback

### getNickForMessage
- Purpose: Retrieves sender nickname for incoming messages
- Calls: gpGetInfo

### getInfoResponseForRequest
- Purpose: Retrieves profile info for buddy requests
- Calls: gpGetInfo

### getInfoResponseForStatus
- Purpose: Retrieves profile info for status updates
- Calls: gpGetInfo

## Globals
- **TheGameSpyBuddyMessageQueue (GameSpyBuddyMessageQueueInterface*)**: Singleton message queue instance

## Dependencies
- GameSpy API (gp*.h functions)
- Threading utilities (ThreadClass, MutexClass)
- Common utilities (string conversion, logging)
- PeerThread.h for cross-thread coordination
