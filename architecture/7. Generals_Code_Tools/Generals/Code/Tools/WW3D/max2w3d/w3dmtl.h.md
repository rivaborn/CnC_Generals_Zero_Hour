# Generals/Code/Tools/WW3D/max2w3d/w3dmtl.h

## Purpose
Defines material-related classes for converting 3D assets between Max and W3D formats.

## Responsibilities
- Define material classes for W3D format
- Handle material conversion from Max materials
- Manage material passes, shaders, textures, and vertex materials
- Provide material remapping and deduplication

## Key Types
- **W3dMapClass (Class)**: Ties map info with filename
- **W3dMaterialClass (Class)**: Manages up to 4 material passes with shaders/textures
- **W3dMaterialDescClass (Class)**: Processes materials, detects duplicates, manages global material info
- **MaterialRemapClass (Class)**: Re-indexes material sub-parts
- **VertMatClass (Class)**: Extends vertex material with pass index and name
- **ShadeClass (Class)**: Extends shader with CRC
- **TexClass (Class)**: Extends texture with CRC
- **ErrorType (Enum)**: Material processing error codes

## Key Functions
### W3dMaterialClass::Init
- Purpose: Initialize material from Max materials
- Calls: None visible

### W3dMaterialDescClass::Add_Material
- Purpose: Add material description and assign index
- Calls: Add_Vertex_Material, Add_Shader, Add_Texture

### W3dMaterialDescClass::Add_Vertex_Material
- Purpose: Add vertex material with deduplication
- Calls: Compute_Crc, Add_String_To_Crc

## Globals
- None

## Dependencies
- "always.h", "w3d_file.h", "vector.h"
- GameMtl, Mtl, ChunkSaveClass (forward declarations)
- W3dTextureInfoStruct, W3dVertexMaterialStruct, W3dShaderStruct (external)
