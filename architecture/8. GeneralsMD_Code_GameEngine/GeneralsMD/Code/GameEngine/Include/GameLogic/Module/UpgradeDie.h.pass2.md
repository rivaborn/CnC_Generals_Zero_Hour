# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/UpgradeDie.h - Enhanced Analysis

## Architectural Role
This file defines a module in the SAGE engine's component-based architecture that handles upgrade removal when an object dies. It extends the `DieModule` base class, integrating with the game's module system to manage object lifecycle events.

## Cross-References
### Incoming
- **GameLogic/Module/DieModule.h**: Base class inheritance
- **Common/INI.h**: For INI field parsing infrastructure
- **Thing.h**: Forward reference for object ownership

### Outgoing
- **DieModuleData::buildFieldParse**: Called during INI parsing setup
- **Upgrade removal logic**: Likely calls into upgrade management systems (not explicitly shown)

## Design Patterns
- **Component Pattern**: `UpgradeDie` is a modular component attached to game objects
- **Strategy Pattern**: `onDie` implements specific behavior for death events
- **INI Parsing Pattern**: Uses `buildFieldParse` for configuration-driven behavior

Rules followed. Output under 400 tokens.
