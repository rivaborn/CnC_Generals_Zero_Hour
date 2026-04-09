# GeneralsMD/Code/GameEngine/Include/GameNetwork/GameSpyGP.h

## Purpose
Header file for GameSpy buddy system integration in Generals Zero Hour.

## Responsibilities
- Declares GameSpy buddy-related callbacks and functions
- Provides access to the global GameSpy connection object
- Exposes buddy status checking functionality

## Key Types
None

## Key Functions
### GPRecvBuddyRequestCallback
- Purpose: Handles incoming buddy requests from GameSpy
- Calls: Not inferable

### GPRecvBuddyMessageCallback
- Purpose: Processes received buddy messages
- Calls: Not inferable

### GPRecvBuddyStatusCallback
- Purpose: Manages buddy status updates
- Calls: Not inferable

### GPErrorCallback
- Purpose: Handles GameSpy connection errors
- Calls: Not inferable

### GPConnectCallback
- Purpose: Manages GameSpy connection responses
- Calls: Not inferable

### GameSpyUpdateBuddyOverlay
- Purpose: Updates the buddy list overlay UI
- Calls: Not inferable

### IsGameSpyBuddy
- Purpose: Checks if a profile ID is a buddy
- Calls: Not inferable

## Globals
- TheGPConnection (GPConnection*): Global pointer to the GameSpy connection

## Dependencies
- GameSpy/GP/GP.h (GPConnection, GPRecvBuddyRequestArg,
