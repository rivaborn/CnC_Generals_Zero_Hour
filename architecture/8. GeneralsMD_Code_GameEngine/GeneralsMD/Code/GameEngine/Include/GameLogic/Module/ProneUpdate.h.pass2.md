# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/ProneUpdate.h - Enhanced Analysis

## Architectural Role
This file defines the prone behavior module within the SAGE engine's component-based architecture. It encapsulates damage-induced cowering logic, bridging the game logic layer with animation and effect systems.

## Cross-References
### Incoming
- **DamageSystem**: Likely calls `goProne()` when damage is applied to prone-capable units
- **AnimationSystem**: May query prone state for animation blending
- **Thing-derived classes**: Instantiate this module via the module system

### Outgoing
- **EffectSystem**: Calls `startProneEffects()`/`stopProneEffects()` to trigger visual/audio cues
- **AnimationSystem**: Implicitly controls prone animations through `update()`
- **ModuleSystem**: Uses base class `UpdateModule` for tick-based updates

## Design Patterns
- **Component Pattern**: Implements prone behavior as a modular attachment to `Thing` objects
- **Strategy Pattern**: Configurable via `ProneUpdateModuleData` for different unit behaviors
- **Observer Pattern**: Reacts to damage events (via `goProne`) to modify state
