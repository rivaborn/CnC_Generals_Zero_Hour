# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/AutoDepositUpdate.cpp - Enhanced Analysis

## Architectural Role
This file implements the economic resource generation system for buildings/units, bridging the game logic layer with player economics and UI feedback. It's a key component in the resource management subsystem, handling both periodic income and upgrade-based modifiers.

## Cross-References
### Incoming
- Called by the game's update loop (via `UpdateModule` base class)
- Used by building/unit object templates that require auto-deposit functionality
- Referenced in INI parsing for upgrade boost configurations

### Outgoing
- Depends on `Player` for money operations
- Uses `TheInGameUI` for visual feedback
- Queries `TheUpgradeCenter` for upgrade state
- Accesses `TheGameLogic` for timing

## Design Patterns
- **Strategy Pattern**: The auto-deposit behavior is encapsulated as a module that can be attached to different object types
- **Observer Pattern**: Listens for game frame updates to trigger deposits
- **Template Method**: Uses `UpdateModule` base class for common update behavior while specializing deposit logic

Rules followed. Output under 400 tokens.
