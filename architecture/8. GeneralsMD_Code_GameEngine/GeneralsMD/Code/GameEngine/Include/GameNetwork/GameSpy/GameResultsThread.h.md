# GeneralsMD/Code/GameEngine/Include/GameNetwork/GameSpy/GameResultsThread.h

## Purpose
Defines interfaces and data structures for handling game results communication via GameSpy in the SAGE engine.

## Responsibilities
- Declares request/response classes for game results data
- Defines abstract interface for game results message queue
- Provides factory method for creating the queue interface
- Manages thread state for game results transmission

## Key Types
- **GameResultsRequest (Class)**: Encapsulates a request to send game results (hostname, port, results data)
- **GameResultsResponse (Class)**: Encapsulates a response from the game results thread (hostname, port, success flag)
- **GameResultsInterface (Class)**: Abstract interface for managing game results message queue and threads

## Key Functions
### GameResultsInterface::createNewGameResultsInterface
- Purpose: Factory method to create a new GameResultsInterface instance
- Calls: Not inferable

### GameResultsInterface::areGameResultsBeingSent
- Purpose: Checks if game results are currently being transmitted
- Calls: Not inferable

## Globals
- **TheGameResultsQueue (GameResultsInterface*)**: Global pointer to the game results message queue interface

## Dependencies
- `Common/SubsystemInterface.h`
- `std::string`
- `UnsignedShort`, `Bool` (custom types)
