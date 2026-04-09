# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/hanim.cpp - Enhanced Analysis

## Architectural Role
This file implements the core animation blending system for the SAGE engine's skeletal animation pipeline. It manages hierarchical animation combinations, pivot weight mapping, and motion blending, serving as the bridge between low-level animation data (HAnimClass) and the rendering hierarchy (HTreeClass).

## Cross-References
### Incoming
- `hmorphanim.cpp` uses `HAnimComboClass::Normalize_Weights` and `NamedPivotMapClass::Update_Pivot_Map` for morph animation blending
- Animation rendering systems likely call into `HAnimComboClass` methods for frame evaluation

### Outgoing
- Calls `HTreeClass` methods (`Get_Bone_Index`, `Num_Pivots`) for bone hierarchy queries
- Uses `HAnimClass` methods (`Get_Num_Pivots`, `Is_Node_Motion_Present`) for animation data access
- Depends on `PivotMapClass` for weight management

## Design Patterns
- **Composite Pattern**: `HAnimComboClass` manages a collection of `HAnimComboDataClass` instances
- **Flyweight Pattern**: Shared animation data via reference counting (`Add_Ref`/`Release_Ref`)
- **Strategy Pattern**: Pivot weight maps as interchangeable strategies for bone influence control
