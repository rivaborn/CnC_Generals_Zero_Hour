# Generals/Code/Tools/WW3D/max2w3d/GameMtl.cpp

## Purpose
Handles material conversion and management for the W3D engine, including parameter blocks, texture stages, and shader properties.

## Responsibilities
- Defines material class descriptor and parameter block structures
- Manages material properties (colors, transparency, shininess)
- Handles texture stage settings (mapping, animation, clamping)
- Provides conversion utilities between material versions
- Supports both PC and PS2 shader parameters

## Key Types
- **GameMaterialClassDesc (Class)**: Material class descriptor for 3DS Max plugin
- **GameMtlPostLoad (Class)**: Handles material post-load conversion
- **PB_* (Enum)**: Parameter block property identifiers
- **Shader_Translation (Enum)**: Shader translation modes
- **ST_* (Enum)**: Blend state translations

## Key Functions
### GameMtlPostLoad::proc
- Purpose: Converts old material formats to current version
- Calls: GameMtl::Set_*, GameMtl::ReplaceReference

### Get_Game_Material_Desc
- Purpose: Returns material class descriptor
- Calls: None

### scale
- Purpose: Scales a value
- Calls: None

## Globals
- **GameMaterialClassID (Class_ID)**: Material class identifier
- **_GameMaterialCD (GameMaterialClassDesc)**: Material class descriptor instance
- **MainParameterBlockDesc (ParamBlockDescID[])**: Main parameter block definition
- **PassParameterBlockDescVer* (ParamBlockDescID[])**: Versioned pass parameter blocks
- **CURRENT_VERSION (int)**: Current parameter block version
- **DISPLACEMENT_INDEX (int)**: Displacement map index

## Dependencies
- gamemtl.h, Max.h, gport.h, hsv.h, GameMtlDlg.h, dllmain.h, resource.h, util.h, meshsave.h, gamemaps.h
- W3dMaterialClass, Texmap, UVGen, ShadeContext, ILoad, PostLoadCallback
