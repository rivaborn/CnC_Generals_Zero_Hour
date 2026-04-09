# Generals/Code/Libraries/Source/WWVegas/WW3D2/dx8fvf.cpp

## Purpose
Handles Flexible Vertex Format (FVF) information for DirectX 8 rendering, including vertex size calculation and FVF name lookup.

## Responsibilities
- Calculate vertex size from FVF flags
- Parse FVF flags to determine offsets for vertex components (position, normal, diffuse, specular, texture coordinates)
- Provide human-readable names for common FVF configurations

## Key Types
- **FVFInfoClass (Class)**: Stores FVF-related offsets and metadata
- **None**: No enums/structs defined

## Key Functions
### Get_FVF_Vertex_Size
- Purpose: Returns the size of a vertex based on its FVF flags
- Calls: D3DXGetFVFVertexSize

### FVFInfoClass::Get_FVF_Name
- Purpose: Converts FVF flags to a human-readable string
- Calls: None

## Globals
- **None**

## Dependencies
- dx8fvf.h (header)
- wwstring.h (StringClass)
- D3dx8core.h (D3DXGetFVFVertexSize, D3DFVF_* flags)
