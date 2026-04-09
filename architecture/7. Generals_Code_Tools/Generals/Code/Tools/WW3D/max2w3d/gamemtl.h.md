# Generals/Code/Tools/WW3D/max2w3d/gamemtl.h

## Purpose
Defines the GameMtl class, a 3DS Max plugin material that emulates the game engine's material system for rendering and parameter control.

## Responsibilities
- Provides material properties and rendering parameters for the game engine
- Manages texture stages, mapping types, and shader parameters
- Supports both PC and PS2 shader types
- Handles material editor integration and parameter blocks
- Implements displacement mapping and material substitution

## Key Types
- **GameMtl (Class)**: Main material class emulating game engine materials
- **ShaderTypeEnum (Enum)**: Defines shader types (PC/PS2)
- **GameMtlDlg (Class)**: Material editor dialog (forward declaration)
- **GameMapsClass (Class)**: Texture mapping class (forward declaration)
- **REF_MAPS/REF_MAIN/REF_PASS_PARAMETERS/REF_TEXTURE/REF_COUNT (Enum)**: Reference indices for material components

## Key Functions
### CreateGameMtl
- Purpose: Factory function to create GameMtl instances
- Calls: Not inferable

### Get_Game_Material_Desc / Get_PS2_Game_Material_Desc / Get_PS2_Material_Conversion
- Purpose: Material class descriptors for 3DS Max plugin system
- Calls: Not inferable

## Globals
- **GameMaterialClassID (Class_ID)**: Class ID for PC game materials
- **PS2GameMaterialClassID (Class_ID)**: Class ID for PS2 game materials
- **PCToPS2MaterialClassID (Class_ID)**: Class ID for material conversion utility

## Dependencies
- `<Max.h>`: 3DS Max SDK headers
- `w3dmtl.h`: W3D material definitions
- `w3d_file.h`: W3D file format definitions
- `Mtl`, `Texmap`, `IParamBlock`, `ShadeContext`: 3DS Max SDK classes
