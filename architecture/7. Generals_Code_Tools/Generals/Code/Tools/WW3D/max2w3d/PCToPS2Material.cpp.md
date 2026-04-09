# Generals/Code/Tools/WW3D/max2w3d/PCToPS2Material.cpp

## Purpose
Converts W3D materials in 3D models to PS2-compatible shaders for the game.

## Responsibilities
- Converts PC shader materials to PS2 shader materials
- Handles both single and multi-materials in 3D models
- Processes all material passes for conversion
- Provides a 3ds Max utility interface for the conversion

## Key Types
- PCToPS2MaterialClass (Class): Main utility class for material conversion
- PCToPS2MaterialClassDesc (Class): Class descriptor for 3ds Max plugin registration
- PCToPS2MaterialClassID (Class_ID): Unique identifier for the utility class

## Key Functions
### PCToPS2MaterialClass::BeginEditParams
- Purpose: Converts all W3D materials in the scene to PS2-compatible shaders
- Calls: GetRootNode, INodeListClass constructor, GetMtl, IsMultiMtl, ClassID, Get_Pass_Count, Compute_PS2_Shader_From_PC_Shader, GetSubMtl, NumSubMtls

### Get_PS2_Material_Conversion
- Purpose: Returns the class descriptor for plugin registration
- Calls: None

## Globals
- PCToPS2MaterialClassID (Class_ID): Unique class identifier
- _PCToPS2MaterialCD (PCToPS2MaterialClassDesc): Static class descriptor instance

## Dependencies
- Max.h, gport.h, hsv.h, dllmain.h, resource.h, util.h, utilapi.h, nodelist.h, gamemtl.h
- INode, Mtl, GameMtl, INodeListClass, GameMaterialClassID, PS2GameMaterialClassID
