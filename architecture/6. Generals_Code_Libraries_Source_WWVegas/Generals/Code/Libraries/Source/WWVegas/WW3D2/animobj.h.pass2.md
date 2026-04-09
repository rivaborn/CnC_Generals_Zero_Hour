# Generals/Code/Libraries/Source/WWVegas/WW3D2/animobj.h - Enhanced Analysis

## Architectural Role
This file defines the core animation system for 3D hierarchical models in the SAGE engine, bridging between the rendering pipeline and animation data structures. It implements the animation state machine and bone transform management, serving as the primary interface for character and vehicle animations.

## Cross-References
### Incoming
- **Rendering System**: Uses `RenderInfoClass` and `SpecialRenderInfoClass` for rendering integration
- **Scene Graph**: Called by scene graph management for transform updates
- **Animation System**: Used by animation controllers and state machines

### Outgoing
- **HTree System**: Directly manipulates `HTreeClass` for bone hierarchy updates
- **Animation Data**: Interfaces with `HAnimClass` and `HAnimComboClass` for motion data
- **Composite Rendering**: Inherits from `CompositeRenderObjClass` for rendering pipeline integration

## Design Patterns
- **State Pattern**: Uses `CurMotionMode` enum with union to manage different animation states (single, blend, combo)
- **Composite Pattern**: Inherits from `CompositeRenderObjClass` for hierarchical object management
- **Strategy Pattern**: Different update methods (`Base_Update`, `Anim_Update`, etc.) act as interchangeable strategies for transform calculation

*Not inferable*: Exact implementation details of animation blending or frame interpolation.
