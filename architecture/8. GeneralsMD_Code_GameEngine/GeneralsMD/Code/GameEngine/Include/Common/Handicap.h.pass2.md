# GeneralsMD/Code/GameEngine/Include/Common/Handicap.h - Enhanced Analysis

## Architectural Role
This file defines the `Handicap` class, which is part of the game's balance system. It provides a mechanism to apply multipliers to game attributes (like build cost and time) based on object types, enabling different difficulty levels or player-specific adjustments.

## Cross-References
### Incoming
- Likely called by game logic systems (e.g., unit/building creation, economy management) to apply balance modifiers.
- May be referenced by AI systems to adjust behavior based on handicap settings.

### Outgoing
- Uses `Dict` for configuration data loading (modding infrastructure).
- Relies on `ThingTemplate` for object type classification (game object hierarchy).

## Design Patterns
- **Strategy Pattern**: The `getHandicap` method selects the appropriate multiplier based on object type, allowing different behaviors without changing the core logic.
- **Data-Driven Design**: Handicap values are loaded from external configuration (`Dict`), enabling modders to adjust game balance without code changes.
- **Enum-Based Dispatch**: Uses enums (`HandicapType`, `ThingType`) to organize and retrieve modifiers efficiently.

(Word count: 198)
