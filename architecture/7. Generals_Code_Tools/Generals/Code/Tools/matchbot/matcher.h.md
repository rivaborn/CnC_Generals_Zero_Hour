# Generals/Code/Tools/matchbot/matcher.h

## Purpose
Defines the `MatcherClass` base class for handling GameSpy matchmaking functionality in the Generals matchbot tool.

## Responsibilities
- Provides virtual hooks for matchmaking events (player joins/leaves, messages, etc.)
- Manages GameSpy peer connection and message handling
- Handles log rotation and configuration
- Abstracts common matchmaking operations

## Key Types
- **MatcherClass (Class)**: Base class for GameSpy matchmaking operations.

## Key Functions
### MatcherClass::handleConnect
- Purpose: Callback for connection success/failure.
- Calls: None visible.

### MatcherClass::handleGroupRoomList
- Purpose: Callback for group room list retrieval.
- Calls: None visible.

### MatcherClass::handleJoin
- Purpose: Callback for room join success/failure.
- Calls: None visible.

### MatcherClass::handleNickError
- Purpose: Callback for nickname errors.
- Calls: None visible.

### MatcherClass::connectAndLoop
- Purpose: Main loop for connection and message handling.
- Calls: `readLoop`.

### MatcherClass::readLoop
- Purpose: Processes incoming GameSpy messages.
- Calls: None visible.

## Globals
- **m_baseNick (Wstring)**: Base nickname for the peer.
- **m_nick (std::string)**: Current nickname.
- **m_profileID (int)**: User profile ID.
- **m_peer (PEER)**: GameSpy peer handle.
- **m_connectSuccess (bool)**: Connection success flag.
- **m_joinSuccess (bool)**: Room join success flag.
- **m_groupID (int)**: Current group ID.
- **m_rotateLogs (bool)**: Log rotation flag.
- **m_lastRotation (time_t)**: Last log rotation time.
- **done (int)**: Loop control flag
