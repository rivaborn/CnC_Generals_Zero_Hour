# GeneralsMD/Code/GameEngine/Include/GameNetwork/GameSpy/PeerDefs.h

## Purpose
Defines core GameSpy peer-to-peer networking structures and interfaces for Generals Zero Hour.

## Responsibilities
- Declares data structures for GameSpy chat, buddy lists, and player info
- Defines color enums for UI elements
- Provides abstract interface for GameSpy functionality
- Declares global functions for GameSpy initialization and chat

## Key Types
- **GameSpyInfoInterface (Class)**: Abstract interface for GameSpy functionality
- **PlayerInfo (Class)**: Stores player statistics and profile data
- **BuddyInfo (Class)**: Contains buddy list information
- **GameSpyColors (Enum)**: Defines color codes for UI elements
- **GameSpyBuddyStatus (Enum)**: Represents buddy online status states

## Key Functions
### WOLDisplayGameOptions
- Purpose: Displays game options in GameSpy interface
- Calls: Not inferable

### WOLDisplaySlotList
- Purpose: Displays player slot list in GameSpy interface
- Calls: Not inferable

### SetUpGameSpy
- Purpose: Initializes GameSpy globals and threads
- Calls: Not inferable

### TearDownGameSpy
- Purpose: Cleans up GameSpy resources
- Calls: Not inferable

## Globals
- **GameSpyColor (Color[GSCOLOR_MAX])**: Array of GameSpy UI colors
- **TheGameSpyInfo (GameSpyInfoInterface**)**: Global GameSpy interface instance

## Dependencies
- "GameSpy/Peer/Peer.h"
- "GameSpy/GP/GP.h"
- "GameClient/Color.h"
- "Common/STLTypedefs.h"
- "GameNetwork/GameSpy/StagingRoomGameInfo.h"
