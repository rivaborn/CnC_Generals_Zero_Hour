# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/Drawable/Draw/W3DSupplyDraw.cpp - Enhanced Analysis

## Architectural Role
This file implements the supply-based bone visibility system for W3D models, bridging the game's supply mechanics with the rendering pipeline. It dynamically adjusts model appearance based on supply levels, a key visual feedback mechanism in Generals/Zero Hour.

## Cross-References
### Incoming
- Called by game logic when supply status changes (e.g., `updateDrawModuleSupplyStatus`)
- Used by model loading system during initialization (`loadPostProcess`)

### Outgoing
- Depends on `W3DModelDraw` base class for core functionality
- Uses `Drawable` interface for bone manipulation
- Leverages `ModelConditionInfo` for bone visibility control

## Design Patterns
- **Template Method**: Extends `W3DModelDraw` with supply-specific behavior while preserving base functionality
- **Strategy**: Encapsulates supply visibility logic as a module that can be attached to different models
- **Observer**: Reacts to supply status changes (implicitly via `updateDrawModuleSupplyStatus` calls)

*Not inferable*: Exact caller relationships or full dependency graph.
