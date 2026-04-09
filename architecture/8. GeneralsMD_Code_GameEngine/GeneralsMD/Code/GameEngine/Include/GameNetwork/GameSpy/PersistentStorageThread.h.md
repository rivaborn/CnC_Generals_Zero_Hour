# GeneralsMD/Code/GameEngine/Include/GameNetwork/GameSpy/PersistentStorageThread.h

## Purpose
Defines interfaces and data structures for GameSpy persistent storage operations in Generals Zero Hour.

## Responsibilities
- Declares classes for player statistics, requests, and responses
- Defines message queue interface for thread communication
- Provides data structures for tracking player stats and game results

## Key Types
- **PSPlayerStats (Class)**: Holds all online-stored player statistics
- **PSRequest (Class)**: Encapsulates a request to the GameSpy thread
- **PSResponse (Class)**: Encapsulates a response from the GameSpy thread
- **GameSpyPSMessageQueueInterface (Class)**: Abstract interface for message queue operations
- **PerGeneralMap (typedef)**: Map type for storing per-general statistics

## Key Functions
### GameSpyPSMessageQueueInterface::createNewMessageQueue
- Purpose: Factory method to create a new message queue instance
- Calls: Not inferable

### GameSpyPSMessageQueueInterface::formatPlayerKVPairs
- Purpose: Converts player stats to key-value pair string format
- Calls: Not inferable

### GameSpyPSMessageQueueInterface::parsePlayerKVPairs
- Purpose: Parses key-value pair string into player stats
- Calls: Not inferable

## Globals
- **TheGameSpyPSMessageQueue (GameSpyPSMessageQueueInterface*)**: Global instance of the message queue

## Dependencies
- `GameSpy/gstats/gpersist.h`
- `std::map`, `std::string` from STL
- Basic types: `Int`, `UnsignedInt`, `Bool`, `Real`
