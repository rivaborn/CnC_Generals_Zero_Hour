# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/animobj.h - Enhanced Analysis

## Architectural Role
This file defines the core animation system for 3D hierarchical models in the SAGE engine, bridging the rendering pipeline (CompositeRenderObjClass) with animation data (HAnimClass). It manages bone transforms and animation blending, critical for character and vehicle animations.

## Cross-References
### Incoming
- **Rendering System**: Uses CompositeRenderObjClass for scene graph integration
- **Animation System**: Consumes HAnimClass and HAnimComboClass for motion data
- **Skin System**: Friend class access indicates tight coupling with SkinClass

### Outgoing
- **Hierarchy System**: Directly manipulates HTreeClass for bone transforms
- **Render Pipeline**: Implements RenderObjClass interface for rendering
- **Transform System**: Uses Matrix3D and Vector3 for spatial calculations

## Design Patterns
- **State Pattern**: Uses CurMotionMode enum to switch between animation states (BASE_POSE, SINGLE_ANIM, etc.)
- **Composite Pattern**: Inherits from CompositeRenderObjClass for hierarchical object management
- **Strategy Pattern**: Different update methods (Base_Update, Anim_Update, etc.) act as interchangeable strategies for transform calculation

*Not inferable*: Exact usage of frameRateMultiplier or dynamic skeleton swapping (Set_HTree)
