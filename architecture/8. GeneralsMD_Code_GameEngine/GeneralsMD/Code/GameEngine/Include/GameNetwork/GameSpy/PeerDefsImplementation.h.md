# GeneralsMD/Code/GameEngine/Include/GameNetwork/GameSpy/PeerDefsImplementation.h

## Purpose
Defines the `GameSpyInfo` class implementation for GameSpy peer (chat) functionality in Generals Zero Hour.

## Responsibilities
- Manages GameSpy group rooms, staging rooms, and player info
- Handles buddy lists, messages, and chat functionality
- Tracks local player profile and connection state
- Manages ignore lists and text filtering

## Key Types
- **GameSpyInfo (Class)**: Main GameSpy peer interface implementation

## Key Functions
### `addGroupRoom`
- Purpose: Adds a group room to the internal map
- Calls: None

### `joinGroupRoom`
- Purpose: Joins a specified group room
- Calls: None

### `addChat`
- Purpose: Adds chat message to registered text windows
- Calls: None

### `sendChat`
- Purpose: Sends chat message to specified player list
- Calls: None

### `addToIgnoreList`
- Purpose: Adds a player to the ignore list
- Calls: None

## Globals
- None

## Dependencies
- `GameNetwork/GameSpy/PeerDefs.h`
- `GameNetwork/GameSpy/PersistentStorageThread.h`
- `AsciiString`, `UnicodeString`, `Color`, `GameWindow` types
- Standard C++ `set` container
