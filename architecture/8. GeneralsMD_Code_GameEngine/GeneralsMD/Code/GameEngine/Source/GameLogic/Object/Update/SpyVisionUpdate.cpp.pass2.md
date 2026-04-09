# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/SpyVisionUpdate.cpp - Enhanced Analysis

## Architectural Role
This file implements the spy vision special power system, which is part of the game's stealth and reconnaissance mechanics. It extends the `UpdateModule` base class to manage vision sharing between players, integrating with the player relationship system and game timing infrastructure.

## Cross-References
### Incoming
- Called by special power activation systems (e.g., spy plane behavior)
- Invoked during player capture events
- Used by object deletion cleanup

### Outgoing
- Calls `Player::setUnitsVisionSpied` to modify vision states
- Uses `TheGameLogic` for frame timing
- Relies on `ThePlayerList` for player iteration

## Design Patterns
- **State Pattern**: Manages active/inactive spy vision states with clear transitions
- **Observer Pattern**: Reacts to game events (capture, deletion) via callback methods
- **Strategy Pattern**: Encapsulates spy vision behavior as a module that can be attached to different objects

Rules followed. Output under 400 tokens.
