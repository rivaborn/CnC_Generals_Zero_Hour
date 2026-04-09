# Generals/Code/Tools/WW3D/max2w3d/PS2GameMtl.cpp

## Purpose
Registers a PS2-specific material class for use in 3DS Max plugin.

## Responsibilities
- Defines PS2GameMaterialClassDesc for PS2 shader materials
- Provides factory function to create PS2 GameMtl instances
- Exposes material type to Max material selector
- Sets shader type to PS2 when creating materials

## Key Types
- PS2GameMaterialClassDesc (Class): ClassDesc-derived descriptor for PS2 materials
- PS2GameMaterialClassID (Class_ID): Unique identifier for PS2 material class

## Key Functions
### Get_PS2_Game_Material_Desc
- Purpose: Returns the PS2 material class descriptor
- Calls: None

### PS2GameMaterialClassDesc::Create
- Purpose: Factory method that creates a new GameMtl with PS2 shader type
- Calls: GameMtl constructor, Set_Shader_Type

## Globals
- PS2GameMaterialClassID (Class_ID): Unique class identifier for PS2 materials
- _PS2GameMaterialCD (PS2GameMaterialClassDesc): Static instance of the class descriptor

## Dependencies
- gamemtl.h (GameMtl class)
- Max.h (3DS Max SDK)
- gport.h (string utilities)
- hsv.h (color utilities)
- dllmain.h (plugin infrastructure)
- resource.h (string IDs)
- util.h (utility functions)
