# GeneralsMD/Code/GameEngine/Source/GameClient/System/CampaignManager.cpp - Enhanced Analysis

## Architectural Role
This file serves as the central hub for campaign progression and state management in the SAGE engine. It bridges the game logic subsystem with the save/load infrastructure, handling both campaign-specific data and challenge mode persistence.

## Cross-References
### Incoming
- **GameClient.h**: Uses `CampaignManager` for mission transitions and state queries
- **ChallengeGenerals.h**: Relies on campaign state for challenge mode continuity
- **GameInfo.h**: Accesses challenge campaign data during serialization

### Outgoing
- **INI.h**: Parses campaign/mission definitions from configuration files
- **Xfer.h**: Handles serialization/deserialization of campaign state
- **GameClient.h**: Triggers mission loading and game state updates

## Design Patterns
- **Singleton Pattern**: `TheCampaignManager` provides global access to campaign state
- **Composite Pattern**: `Campaign` contains a list of `Mission` objects
- **Visitor Pattern**: `FieldParse` table drives INI parsing via reflection-like mechanism

*Not inferable*: Exact usage of `Xfer` for versioned serialization.
