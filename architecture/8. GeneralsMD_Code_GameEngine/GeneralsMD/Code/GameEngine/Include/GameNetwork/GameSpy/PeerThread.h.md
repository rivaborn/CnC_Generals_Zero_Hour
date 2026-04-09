# GeneralsMD/Code/GameEngine/Include/GameNetwork/GameSpy/PeerThread.h

## Purpose
Defines interfaces and data structures for GameSpy peer-to-peer networking in Generals Zero Hour.

## Responsibilities
- Declares request/response message structures for peer communication
- Defines thread management interface for GameSpy peer operations
- Specifies enums for connection states and quick match statuses
- Provides global message queue singleton access

## Key Types
- **SerialAuthResult (Enum)**: Serial number authentication status
- **PeerRequest (Class)**: Encapsulates client requests to peer thread
- **DisconnectReason (Enum)**: Reasons for disconnection
- **QMStatus (Enum)**: Quick match operation states
- **PeerResponse (Class)**: Encapsulates responses from peer thread
- **GameSpyPeerMessageQueueInterface (Class)**: Abstract message queue interface

## Key Functions
### createNewMessageQueue
- Purpose: Factory method to create message queue instance
- Calls: Not inferable

## Globals
- **TheGameSpyPeerMessageQueue (GameSpyPeerMessageQueueInterface*)**: Global message queue instance

## Dependencies
- "GameSpy/Peer/Peer.h"
- "GameNetwork/NetworkDefs.h"
- std::string, std::wstring, std::vector
