# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/CommandButtonHuntUpdate.h - Enhanced Analysis

## Architectural Role
This file defines a specialized update module for wounded infantry units, bridging the AI behavior system with the command button interface. It extends the generic `UpdateModule` to implement targeted hunting logic for healing, integrating with the game's command system and spatial query mechanisms.

## Cross-References
### Incoming
- AI behavior system (calls `huntSpecialPower`, `huntWeapon`, `huntEnter`)
- Command button system (calls `setCommandButton`)
- Spatial query system (calls `scanClosestTarget`)

### Outgoing
- `ModuleData` hierarchy for configuration
- `Thing` and `CommandButton` for game object interactions
- `AIUpdateInterface` for behavior updates

## Design Patterns
- **Strategy Pattern**: The hunt methods (`huntSpecialPower`, `huntWeapon`, `huntEnter`) encapsulate different hunting behaviors, allowing dynamic selection.
- **Template Method**: `update()` likely delegates to specific hunt methods, defining a skeleton algorithm.
- **Dependency Injection**: `CommandButtonHuntUpdateModuleData` injects configuration (scan range/frames) into the module.
