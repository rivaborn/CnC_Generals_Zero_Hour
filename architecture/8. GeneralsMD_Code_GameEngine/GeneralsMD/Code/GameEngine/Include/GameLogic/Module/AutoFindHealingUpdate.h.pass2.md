# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/AutoFindHealingUpdate.h - Enhanced Analysis

## Architectural Role
This file defines a specialized update module for the SAGE engine's behavior system, specifically handling wounded infantry healing logic. It integrates with the game's object update framework to periodically scan for healing targets, demonstrating the engine's modular behavior system architecture.

## Cross-References
### Incoming
- Likely called by the game's object update manager (not explicitly shown in header)
- May be referenced in infantry unit templates that require healing behavior

### Outgoing
- Uses `UpdateModule` base class for update timing
- Depends on `ModuleData` for configuration
- Forward references suggest interaction with `ThingTemplate` and `WeaponTemplate` systems

## Design Patterns
- **Module Pattern**: Encapsulates healing behavior as a reusable component
- **Strategy Pattern**: Implements healing logic as an interchangeable update strategy
- **Configuration Pattern**: Uses `ModuleData` for externalized behavior parameters

Rules followed. Output under 400 tokens.
