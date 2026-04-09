# GeneralsMD/Code/GameEngine/Source/Common/RTS/Team.cpp - Enhanced Analysis

## Architectural Role
This file implements the core team management system, acting as a bridge between game objects and higher-level game logic. It handles team creation, relations, and member operations, while also managing serialization for save/load functionality.

## Cross-References
### Incoming
- Game logic systems (e.g., AI, scripting) call team functions for member operations
- Player systems query team relations for gameplay decisions
- Save/load systems use team serialization methods

### Outgoing
- Calls into Object system for member operations (recruitment, killing)
- Uses ScriptEngine for team-specific script execution
- Interacts with PartitionManager for spatial queries
- Depends on PlayerList for neutral player lookups

## Design Patterns
- **Factory Pattern**: TeamFactory manages team creation and lookup
- **Observer Pattern**: Team maintains relations maps that notify when relationships change
- **Serialization Pattern**: Custom xfer methods handle save/load with versioning support

Rules followed. Output under 400 tokens.
