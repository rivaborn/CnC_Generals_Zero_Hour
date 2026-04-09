# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/animobj.cpp - Enhanced Analysis

## Architectural Role
This file implements the core animation system for 3D objects in the SAGE engine, bridging the rendering pipeline (WW3D) with animation data (HAnim/HCAAnim) and bone hierarchies (HTree). It handles the temporal progression of animations, bone transformations, and state management for all animated game entities.

## Cross-References
### Incoming
- **Rendering Pipeline**: `Render` is called by the WW3D rendering system during frame updates.
- **Game Logic**: Unit/building controllers call `Set_Animation` to trigger specific animations (e.g., attack, idle).
- **UI System**: Cutscene or cinematic playback systems likely invoke animation control methods.

### Outgoing
- **Animation Data**: Relies on `HAnimClass`/`HCAAnimClass` for motion data and `HTreeClass` for bone hierarchies.
- **Asset Management**: Uses `WW3DAssetManager` to load HTree assets.
- **Audio System**: Triggers `AnimatedSoundMgrClass` for animation-linked sounds.
- **Math Library**: Uses `WWMath` for transform calculations.

## Design Patterns
- **State Pattern**: Animation modes (`SINGLE_ANIM`, `BLEND_ANIM`, etc.) are implemented as distinct state behaviors with shared interfaces.
- **Composite Pattern**: `Animatable3DObjClass` inherits from `CompositeRenderObjClass`, allowing hierarchical object management.
- **Observer Pattern**: Animation frame changes notify dependent systems (e.g., sound triggers) via `Single_Anim_Progress`.

*Not inferable*: Exact implementation of `AnimComboClass` or memory management for motion assets.
