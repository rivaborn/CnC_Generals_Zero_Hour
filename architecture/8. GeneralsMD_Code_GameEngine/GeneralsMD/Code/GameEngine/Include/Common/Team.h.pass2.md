# GeneralsMD/Code/GameEngine/Include/Common/Team.h - Enhanced Analysis

## Architectural Role
This file defines the core team system, bridging game logic (team behavior, relationships) and AI (team creation, scripting). It serves as the central authority for team identity, membership, and inter-team dynamics, with tight coupling to the player system and scripting engine.

## Cross-References
### Incoming
- **AI System**: Uses `TeamFactory` for dynamic team creation during gameplay
- **Player System**: Calls `friend_setOwningPlayer` to establish team ownership
- **Scripting Engine**: Executes team-specific scripts via `getGenericScript`

### Outgoing
- **Snapshot System**: Inherits from `Snapshot` for serialization/deserialization
- **Memory Pool**: Uses `MemoryPoolObject` for object lifecycle management
- **Object System**: Iterates over team members via `ObjectIterateFunc`

## Design Patterns
- **Factory Pattern**: `TeamFactory` centralizes team prototype management and instantiation
- **Composite Pattern**: Teams contain members (objects) and can form hierarchies (subteams)
- **Observer Pattern**: Scripts attached to teams react to game events (e.g., `m_scriptOnEnemySighted`)

*Not inferable*: Exact implementation of `TeamRelationMap` (e.g., whether it uses flyweight for relationships).
