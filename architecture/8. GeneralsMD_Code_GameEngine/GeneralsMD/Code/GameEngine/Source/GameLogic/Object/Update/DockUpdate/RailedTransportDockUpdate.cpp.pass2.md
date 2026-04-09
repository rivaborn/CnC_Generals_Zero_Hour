# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/DockUpdate/RailedTransportDockUpdate.cpp - Enhanced Analysis

## Architectural Role
This file implements the docking behavior for railed transport vehicles, extending the base `DockUpdate` class. It handles the mechanical process of loading/unloading objects via timed movement along predefined paths, integrating with the containment system and AI modules.

## Cross-References
### Incoming
- Called by the game's update loop (via `Update` base class)
- Used by AI modules when issuing dock/undock commands
- Referenced in object template definitions for railed transports

### Outgoing
- Interacts with `ContainModule` and `OpenContain` for object containment
- Uses `AIUpdate` for movement commands
- Relies on `PartitionManager` for object lookup
- Depends on `Drawable` for model state changes

## Design Patterns
- **Template Method**: Extends `DockUpdate::update()` with specialized docking logic
- **State Machine**: Implicit state handling for docking phases (pull-in/push-out)
- **Dependency Injection**: Receives module data via constructor parameter

*Not inferable*: Exact pattern usage in `getFirstContain` callback.
