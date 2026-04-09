# Generals/Code/Libraries/Source/WWVegas/WW3D2/hanim.cpp - Enhanced Analysis

## Architectural Role
This file implements the core animation blending system for the W3D renderer, enabling hierarchical skeletal animation with per-bone weight control. It bridges between the animation data (HAnim) and the rendering hierarchy (HTree), providing the mathematical foundation for motion blending used throughout character and vehicle animations.

## Cross-References
### Incoming
- `hmorphanim.cpp` uses `HAnimComboClass::Normalize_Weights` for morph animation blending
- `hmorphanim.cpp` references `NamedPivotMapClass::Update_Pivot_Map` for bone weight mapping

### Outgoing
- Calls into `HTreeClass` methods (`Num_Pivots()`, `Get_Bone_Index()`) for skeleton hierarchy access
- Uses `HAnimClass` methods (`Get_Num_Pivots()`, `Is_Node_Motion_Present()`) for animation data interrogation
- Depends on `WWMath` for floating-point operations and epsilon comparisons

## Design Patterns
- **Composite Pattern**: `HAnimComboClass` manages a collection of `HAnimComboDataClass` instances, treating each as a component in the animation blend
- **Flyweight Pattern**: Uses reference counting (`Add_Ref()`, `Release_Ref()`) and shared data flags to optimize memory usage for animation assets
- **Strategy Pattern**: Pivot weight maps (`PivotMapClass`) are interchangeable strategies for controlling bone influence during blending

*Not inferable*: Exact implementation of `PivotMapClass` hierarchy or how `HAnimComboClass` integrates with the game's animation state machine.
