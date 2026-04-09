# Generals/Code/GameEngine/Source/GameNetwork/NAT.cpp

## Purpose
Handles NAT traversal and connection negotiation between players in a multiplayer game.

## Responsibilities
- Manages connection pairing and round-based negotiation
- Handles probe packets and port mangling for NAT traversal
- Tracks connection states and retries
- Notifies users of connection success/failure
- Processes global messages for NAT coordination

## Key Types
- NAT (Class): Main NAT traversal manager
- NATStateType (Enum): NAT operation states (IDLE, DONE, etc.)
- NATConnectionState (Enum): Connection states (WAITINGFORRESPONSE, DONE, etc.)
- MS_TO_WAIT_FOR_STATS (Enum): Timeout constant (5000ms)

## Key Functions
### update
- Purpose: Updates NAT state and connection negotiation
- Calls: allConnectionsDoneThisRound, doThisConnectionRound, connectionUpdate, notifyUsersOfConnectionFailed, endMenu

### connectionUpdate
- Purpose: Updates transport and handles probe/keepalive packets
- Calls: sendMangledPortNumberToTarget, queueSend, update, sendAProbe, notifyTargetOfProbe, notifyUsersOfConnectionDone

### processGlobalMessage
- Purpose: Processes incoming NAT coordination messages
- Calls: probed, setConnectionState, gotInternalAddress, gotMangledPort

### notifyUsersOfConnectionDone/notifyUsersOfConnectionFailed
- Purpose: Sends connection status notifications to other players
- Calls: addRequest

## Globals
- TheNAT (NAT*): Global NAT instance
- m_connectionPairs (Int[]): Predefined connection pairing schemes
- m_timeBetweenRetries (Int): Retry interval (500ms)
- m_keepaliveInterval (time_t): Keepalive interval (15s)
- m_timeForRoundTimeout (time_t): Round timeout (15s)

## Dependencies
- GameNetwork/NAT.h, Transport.h, NetworkDefs.h
- GameClient/EstablishConnectionsMenu.h
- GameNetwork/GameInfo.h
- GameNetwork/GameSpy/PeerThread.h, PeerDefs.h, PersistentStorageThread.h, GSConfig.h
