# GeneralsMD/Code/GameEngine/Source/Common/RTS/AcademyStats.cpp - Enhanced Analysis

## Architectural Role
This file implements the in-game "Academy" system, which tracks player performance metrics and generates contextual advice. It bridges the gap between player behavior analysis and UI feedback, operating as a middleware layer between core game logic and the control bar.

## Cross-References
### Incoming
- **GameClient/ControlBar.cpp**: Uses `findDozerCommandSet` to locate dozer command sets
- **GameLogic/GameLogic.cpp**: Likely calls `update` during game frame processing
- **Networking/Xfer.cpp**: Calls `xfer` for serialization during save/load or network sync

### Outgoing
- **GameClient/ControlBar.h**: Accesses `TheControlBar` for command set queries
- **GameClient/GameText.h**: Uses `TheGameText` for localized advice strings
- **Common/Player.h**: Iterates player objects and checks templates
- **GameLogic/GameLogic.h**: Gets current frame via `TheGameLogic`

## Design Patterns
- **Observer Pattern**: Tracks player actions by iterating objects and recording events
- **Data-Driven Design**: Advice generation uses tiered stats (1-3) with conditional checks
- **Serialization Proxy**: `xfer` method handles network/savegame sync of stats

*Not inferable*: Exact advice generation logic (truncated in sample)
