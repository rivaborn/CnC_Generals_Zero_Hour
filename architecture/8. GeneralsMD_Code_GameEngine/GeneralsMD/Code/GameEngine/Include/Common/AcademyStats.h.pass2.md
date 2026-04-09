# GeneralsMD/Code/GameEngine/Include/Common/AcademyStats.h - Enhanced Analysis

## Architectural Role
This file defines the `AcademyStats` class, which serves as the engine's player behavior analytics system. It tracks in-game actions (buildings, upgrades, special powers) and generates contextual advice for players, integrating with the UI and player progression systems.

## Cross-References
### Incoming
- **UI Systems**: Likely called by the in-game advice/academy UI to fetch tips
- **Player Systems**: Called by player/unit management when recording actions (e.g., `recordProduction`)
- **Game Logic**: Used by mission/strategy systems to evaluate player performance

### Outgoing
- **Snapshot System**: Uses `Snapshot` base class for serialization
- **Template Systems**: References `ThingTemplate`, `UpgradeTemplate`, etc. for game data
- **Player Systems**: Accesses `Player` data for context-aware advice

## Design Patterns
- **Observer Pattern**: Tracks player actions without direct control (passive recording)
- **Strategy Pattern**: Tiered advice evaluation (`evaluateTier1Advice`, etc.) acts as interchangeable strategies
- **Data Capsule**: Encapsulates player statistics with controlled access via methods

*Not inferable*: Exact UI integration or advice delivery mechanism.
