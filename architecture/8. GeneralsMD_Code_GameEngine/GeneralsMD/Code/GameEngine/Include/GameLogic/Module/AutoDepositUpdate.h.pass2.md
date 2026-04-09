# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/AutoDepositUpdate.h - Enhanced Analysis

## Architectural Role
This file defines the `AutoDepositUpdate` module, which is part of the game's resource management system. It handles periodic resource deposits for players, initial capture bonuses, and upgrade-based supply boosts, integrating with the broader economy and player progression systems.

## Cross-References
### Incoming
- **Player Management**: Likely called by player-related systems when capturing structures or managing resources.
- **Thing System**: Used by game objects (Things) that need to deposit resources (e.g., supply depots).
- **INI Parsing**: Called during game initialization to parse configuration data for deposit rules.

### Outgoing
- **UpdateModule**: Inherits from `UpdateModule`, so it calls into the update system for periodic execution.
- **Player Economy**: Modifies player resources (money/credits) via `awardInitialCaptureBonus`.
- **Upgrade System**: Uses `getUpgradedSupplyBoost` to query upgrade effects, likely from a global upgrade manager.

## Design Patterns
- **Module Pattern**: Encapsulates resource deposit logic as a reusable module attached to game objects.
- **Strategy Pattern**: The `update` method acts as a strategy for timed resource generation, decoupled from the Thing's core behavior.
- **Data-Driven Design**: Uses `buildFieldParse` to load configuration from INI files, allowing modders to tweak deposit rules without code changes.
