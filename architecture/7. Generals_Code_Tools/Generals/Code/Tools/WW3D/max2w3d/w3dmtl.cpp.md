# Generals/Code/Tools/WW3D/max2w3d/w3dmtl.cpp

## Purpose
Handles material and texture conversion for 3D models in the Max2W3d tool, bridging 3DS Max materials to W3D format.

## Responsibilities
- Manages W3dMapClass (texture maps) and W3dMaterialClass (materials)
- Converts 3DS Max material properties to W3D format
- Handles texture references and animation info
- Implements material indexing and deduplication via CRC hashing

## Key Types
- W3dMapClass (Class): Represents texture maps with filename and animation info
- W3dMaterialClass (Class): Manages material passes, shaders, textures, and vertex materials
- W3dMaterialDescClass (Class): Handles material collection, indexing, and querying
- W3dRGBStruct (Struct): RGB color representation for W3D

## Key Functions
### Color_To_W3d
- Purpose: Converts 3DS Max Color to W3D RGB format
- Calls: None

### W3dMaterialClass::Init
- Purpose: Initializes material from 3DS Max Mtl object
- Calls: W3d_Shader_Reset, Set_Texture, etc.

### W3dMaterialDescClass::Add_Vertex_Material
- Purpose: Adds vertex material to collection with CRC deduplication
- Calls: Compute_Crc, Add_String_To_Crc

### W3dMaterialDescClass::Compute_Crc
- Purpose: Generates CRC hash for material components
- Calls: CRC_Memory, CRC_Stringi, Add_String_To_Crc

## Globals
- None

## Dependencies
- w3dmtl.h, Max.h, StdMat.h, gamemtl.h, realcrc.h
- W3D shader functions (W3d_Shader_Reset, etc.)
- 3DS Max material system (Mtl, GameMtl)
- CRC functions (CRC_Memory, CRC_Stringi)
