# Generals/Code/Libraries/Source/WWVegas/WW3D2/animobj.cpp - Enhanced Analysis

## Architectural Role
This file implements the core animation system for 3D objects in the SAGE engine, bridging the rendering pipeline (WW3D) with the asset management system. It handles the runtime animation state machine, bone hierarchy transformations, and animation blending/playback logic that drives character and vehicle animations in-game.

## Cross-References
### Incoming
- **Rendering System**: `Render()` called during the WW3D render pipeline
- **Game Logic**: Unit/vehicle classes call `Set_Animation()` to trigger specific animations
- **AI System**: Behavior scripts likely invoke `Is_Animation_Complete()` for animation-driven actions

### Outgoing
- **Asset Management**: Uses `WW3DAssetManager` to load HTree and HAnim assets
- **Math Library**: Relies on `WWMath` for transform calculations
- **Memory System**: Uses `WWMEMLOG` for memory tracking
- **Debug System**: Calls `WWDEBUG_SAY` for error reporting

## Design Patterns
- **State Pattern**: Animation modes (SINGLE_ANIM, INTERP_ANIM, etc.) act as states with different behaviors
- **Composite Pattern**: `Animatable3DObjClass` inherits from `CompositeRenderObjClass`, suggesting hierarchical object management
- **Strategy Pattern**: Different animation update methods (`Anim_Update`, `Blend_Update`) are selected based on current state

*Not inferable*: Exact implementation of `Combo_Update` or how animation blending weights are calculated.
