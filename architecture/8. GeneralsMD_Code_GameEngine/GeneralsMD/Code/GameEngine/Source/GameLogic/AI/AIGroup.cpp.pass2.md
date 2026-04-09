# GeneralsMD/Code/GameEngine/Source/GameLogic/AI/AIGroup.cpp - Enhanced Analysis

## Architectural Role
This file implements the AIGroup class, which acts as a container for AI-controlled objects, coordinating their collective behavior within the AI subsystem. It bridges between individual unit AI (via AIUpdate modules) and higher-level AI strategies, handling group movement, command delegation, and state synchronization.

## Cross-References
### Incoming
- **AI.cpp**: Uses AIGroup for pathfinding and behavior coordination
- **ActionManager.cpp**: Queries groups for special power sources
- **ControlBar.cpp**: Retrieves command button sources for UI feedback
- **SpecialPowerModule.cpp**: Delegates special power execution to group members

### Outgoing
- **AIPathfind.cpp**: Uses pathfinding utilities for group movement
- **AIUpdate.h**: Interfaces with individual unit AI modules
- **SpecialPowerUpdateModule.h**: Manages special power overrides
- **Xfer.h/XferCRC.h**: Handles network synchronization and CRC generation

## Design Patterns
- **Composite Pattern**: Groups treat collections of units as single logical entities
- **Observer Pattern**: Group state changes propagate to members via module interfaces
- **Strategy Pattern**: Command delegation uses command button types to determine appropriate actions

*Not inferable*: Exact implementation of pathfinding delegation or command resolution strategy.
