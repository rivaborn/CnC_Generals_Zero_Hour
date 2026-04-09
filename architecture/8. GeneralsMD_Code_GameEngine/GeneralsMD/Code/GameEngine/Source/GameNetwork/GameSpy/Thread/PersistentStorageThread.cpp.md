# GeneralsMD/Code/GameEngine/Source/GameNetwork/GameSpy/Thread/PersistentStorageThread.cpp

## Purpose
Manages communication with GameSpy's persistent storage server via a dedicated thread and message queue.

## Responsibilities
- Handles player statistics tracking and retrieval
- Manages authentication and data synchronization with GameSpy servers
- Provides thread-safe message passing between game logic and network operations
- Parses and formats player statistics data for storage/retrieval

## Key Types
- **PSRequest (Class)**: Represents a request to the GameSpy server
- **PSResponse (Class)**: Represents a response from the GameSpy server
- **PSThreadClass (Class)**: The worker thread handling GameSpy communication
- **GameSpyPSMessageQueue (Class)**: Message queue interface for thread-safe communication
- **PSPlayerStats (Struct)**: Contains player statistics data
- **CDAuthInfo (Class)**: CD authentication information

## Key Functions
### debugDumpPlayerStats
- Purpose: Logs player statistics for debugging
- Calls: None

### persAuthCallback
- Purpose: Handles persistent authentication callback
- Calls: Not inferable

### getPersistentDataCallback
- Purpose: Handles retrieval of persistent data callback
- Calls: Not inferable

### setPersistentDataLocaleCallback
- Purpose: Handles setting locale for persistent data callback
- Calls: Not inferable

### setPersistentDataCallback
- Purpose: Handles setting persistent data callback
- Calls: Not inferable

### preAuthCDCallback
- Purpose: Handles CD pre-authentication callback
- Calls: Not inferable

### getPreorderCallback
- Purpose: Handles pre-order data retrieval callback
- Calls: Not inferable

## Globals
- **TheGameSpyPSMessageQueue (GameSpyPSMessageQueue**)**: Global instance of the message queue

## Dependencies
- "PreRTS.h", "Common/UserPreferences.h", "Common/PlayerTemplate.h", "GameNetwork/GameSpy/PersistentStorageThread.h", "GameNetwork/GameSpy/PeerDefs.h", "mutex.h", "thread.h", "Common/StackDump.h", "Common/SubsystemInterface.h"
