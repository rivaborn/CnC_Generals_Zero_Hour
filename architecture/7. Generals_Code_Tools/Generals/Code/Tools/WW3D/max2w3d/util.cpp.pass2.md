# Generals/Code/Tools/WW3D/max2w3d/util.cpp - Enhanced Analysis

## Architectural Role
This file serves as the utility layer for the Max-to-W3D exporter, providing core functionality for node hierarchy manipulation, naming conventions, and geometric validation. It bridges the 3DS Max SDK with the W3D export pipeline, handling the semantic translation between Max's scene graph and the engine's expected structure.

## Cross-References
### Incoming
- `w3dutil.cpp` (calls `Set_W3D_Name`, `Split_Node_Name`, `Is_Max_Tri_Mesh`, `Is_Damage_Root`, `Is_Origin`, `Is_Base_Origin`, `Get_Lod_Level`, `Get_Damage_State`, `Find_Named_Node`)
- Likely called by other exporter tools or Max script interfaces (not explicitly referenced in provided context)

### Outgoing
- Directly uses 3DS Max SDK classes (`INode`, `Object`, `Matrix3`)
- Relies on `W3DAppData2Struct` for geometry metadata (engine-specific wrapper)
- Uses standard C runtime functions (`strrchr`, `sscanf`, etc.)

## Design Patterns
- **Naming Convention Enforcer**: Functions like `Set_W3D_Name` and `Split_Node_Name` enforce strict naming rules for W3D compatibility, acting as a translation layer between Max's flexible naming and the engine's rigid requirements.
- **Hierarchy Traversal**: `Find_Named_Node` implements breadth-first search for node lookup, typical of scene graph operations in asset pipelines.
- **State Extraction**: Functions like `Get_Lod_Level` and `Get_Damage_State` use naming patterns to derive runtime state, embedding metadata in the hierarchy structure (a common asset pipeline technique).
