# GeneralsMD/Code/GameEngine/Include/GameNetwork/GameSpy/BuddyThread.h

## Purpose
Defines interfaces for GameSpy buddy list functionality, including request/response structures and message queue management.

## Responsibilities
- Defines `BuddyRequest` and `BuddyResponse` classes for buddy list operations
- Declares `GameSpyBuddyMessageQueueInterface` for thread-safe message passing
- Provides global access to the buddy message queue via `TheGameSpyBuddyMessageQueue`

## Key Types
- **BuddyRequest (Class)**: Encapsulates buddy list operation requests (login, message, add buddy, etc.)
- **BuddyResponse (Class)**: Encapsulates responses from the buddy thread to the UI
- **GameSpyBuddyMessageQueueInterface (Class)**: Abstract interface for managing buddy list message queues
- **TheGameSpyBuddyMessageQueue (Global)**: Singleton instance of the message queue interface

## Key Functions
### `createNewMessageQueue`
- Purpose: Factory method to create a new message queue instance
- Calls: Not inferable

## Globals
- **TheGameSpyBuddyMessageQueue (GameSpyBuddyMessageQueueInterface*)**: Global pointer to the buddy message queue instance

## Dependencies
- `GameSpy/GP/GP.h` (GameSpy SDK headers)
- `GPProfile`, `GPResult`, `GPErrorCode`, `GPEnum` (GameSpy types)
