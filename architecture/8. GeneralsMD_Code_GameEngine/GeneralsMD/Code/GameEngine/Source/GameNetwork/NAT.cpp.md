# GeneralsMD/Code/GameEngine/Source/GameNetwork/NAT.cpp

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
- NATConnectionState (Enum): Connection state (e.g., waiting, done, failed)
- NATStateType (Enum): Overall NAT state (idle, negotiating, done, failed)
- MS_TO_WAIT_FOR_STATS (Enum): Timeout for waiting for player stats

## Key Functions
### update
- Purpose: Updates NAT state and connection negotiation
- Calls: allConnectionsDoneThisRound, allConnectionsDone, doThisConnectionRound, connectionUpdate, notifyUsersOfConnectionFailed, TheEstablishConnectionsMenu->endMenu

### connectionUpdate
- Purpose: Updates transport and checks for probe responses
- Calls: sendMangledPortNumberToTarget, m_transport->update, sendAProbe, notifyTargetOfProbe, notifyUsersOfConnectionDone

### processGlobalMessage
- Purpose: Processes NAT-related messages from other players
- Calls: probed, setConnectionState, gotInternalAddress, gotMangledPort

### notifyUsersOfConnectionDone
- Purpose: Notifies users when a connection is established
- Calls: TheGameSpyPeerMessageQueue->addRequest

### notifyUsersOfConnectionFailed
- Purpose: Notifies users when a connection fails
- Calls: TheGameSpyPeerMessageQueue->addRequest

## Globals
- TheNAT (NAT*): Global NAT instance
- m_connectionPairs (Int[]): Predefined connection pairing schemes
- m_timeBetweenRetries (Int): Retry interval in milliseconds
- m_manglerRetryTimeInterval (time_t): Mangler retry interval
- m_maxAllowedManglerRetries (Int): Maximum mangler retries
- m_keepaliveInterval (time_t): Keepalive packet interval
- m_timeToWaitForPort (time_t): Timeout for waiting for port
- m_timeForRoundTimeout (time_t): Timeout for connection round

## Dependencies
- GameNetwork/NAT.h, Transport.h, NetworkDefs.h
- GameClient/EstablishConnectionsMenu.h
- GameNetwork/NetworkInterface.h, GameInfo.h
- GameNetwork/GameSpy/PeerThread.h, PeerDefs.h, PersistentStorageThread.h, GSConfig.h
