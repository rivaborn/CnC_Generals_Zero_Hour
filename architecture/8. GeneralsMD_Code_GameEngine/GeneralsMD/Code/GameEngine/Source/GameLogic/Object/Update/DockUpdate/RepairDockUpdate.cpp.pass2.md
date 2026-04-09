# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/DockUpdate/RepairDockUpdate.cpp - Enhanced Analysis

## Architectural Role
This file implements the repair docking behavior in the game's object update system. It extends the base `DockUpdate` class to handle health restoration for units docked at repair structures, integrating with the game's damage/healing system and networking infrastructure.

## Cross-References
### Incoming
- **GameLogic/Object/Update/DockUpdate/DockUpdate.cpp**: Calls `RepairDockUpdate::action` during docking updates
- **GameLogic/Module/BodyModule.cpp**: Invoked via `getBodyModule()` for health management
- **Networking/Xfer.cpp**: Uses `xferObjectID` and `xferReal` for serialization

### Outgoing
- **GameLogic/Object/Update/DockUpdate/DockUpdate.cpp**: Inherits from `DockUpdate`
- **GameLogic/Module/BodyModule.cpp**: Calls `attemptHealing` for health restoration
- **Common/Xfer.cpp**: Uses `Xfer` methods for networking

## Design Patterns
- **Template Method**: Extends `DockUpdate` with specialized repair logic in `action()`
- **Data Transfer Object**: `RepairDockUpdateModuleData` encapsulates repair configuration
- **State Pattern**: Tracks repair state via `m_lastRepair` and `m_healthToAddPerFrame`
