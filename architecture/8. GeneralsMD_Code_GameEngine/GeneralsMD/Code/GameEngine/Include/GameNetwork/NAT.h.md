# GeneralsMD/Code/GameEngine/Include/GameNetwork/NAT.h

## Purpose
Manages NAT traversal for multiplayer connections in Generals/Zero Hour.

## Responsibilities
- Resolves NAT'd IPs and port numbers for game slots
- Coordinates connection paths between players
- Handles NAT state transitions and timeouts
- Processes GameSpy notifications for NAT traversal

## Key Types
- **NATStateType (Enum)**: NAT traversal state (IDLE, DOCONNECTIONPATHS, WAITFORSTATS, DONE, FAILED)
- **NATConnectionState (Enum)**: Connection state per node (NOSTATE, WAITINGTOBEGIN, WAITINGFORMANGLERRESPONSE, etc.)
- **ConnectionNodeType (Struct)**: Stores NAT behavior and slot index for a connection node
- **NAT (Class)**: Main NAT traversal manager class

## Key Functions
### update
- Purpose: Updates NAT traversal state machine
- Calls: connectionUpdate, allConnectionsDone, doThisConnectionRound

### establishConnectionPaths
- Purpose: Initiates NAT traversal process
- Calls: Not inferable

### processGlobalMessage
- Purpose: Handles GameSpy NAT traversal notifications
- Calls: Not inferable

### connectionUpdate
- Purpose: Updates connection state for current round
- Calls: allConnectionsDoneThisRound, sendMangledSourcePort, processManglerResponse

### sendMangledSourcePort
- Purpose: Starts mangled port acquisition process
- Calls: Not inferable

## Globals
- **TheNAT (NAT*)**: Singleton instance of NAT manager

## Dependencies
- "Lib/BaseType.h"
- "GameNetwork/NetworkInterface.h"
- "GameNetwork/FirewallHelper.h"
- Transport class
- GameSlot class
- FirewallHelperClass
