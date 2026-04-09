# Generals/Code/Tools/WW3D/max2w3d/PCToPS2Material.cpp - Enhanced Analysis

## Architectural Role
This file implements a 3ds Max utility plugin for converting W3D material shaders from PC to PS2 format during the asset pipeline. It bridges the 3D modeling tool (3ds Max) with the game's W3D renderer, ensuring cross-platform material compatibility.

## Cross-References
### Incoming
- Called by 3ds Max plugin infrastructure when the utility is invoked
- Likely referenced by other max2w3d tools that need material conversion

### Outgoing
- Calls into `GameMtl` class methods (`Compute_PS2_Shader_From_PC_Shader`, `Get_Pass_Count`)
- Uses 3ds Max SDK (`INode`, `Mtl`, `INodeListClass`)
- Depends on `gamemtl.h` for material class definitions

## Design Patterns
- **Plugin Architecture**: Implements 3ds Max utility plugin pattern with `ClassDesc` registration
- **Visitor Pattern**: Iterates through scene graph nodes to apply transformations (material conversion)
- **Factory Method**: `Create()` method in `ClassDesc` for object instantiation

*Not inferable*: Exact shader conversion algorithm details or PS2-specific shader constraints.
