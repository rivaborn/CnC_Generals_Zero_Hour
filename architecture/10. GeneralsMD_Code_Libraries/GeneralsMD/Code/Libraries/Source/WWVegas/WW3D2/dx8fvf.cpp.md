# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/dx8fvf.cpp

## Purpose
Handles Flexible Vertex Format (FVF) information for DirectX 8 rendering, including vertex size calculation and offset management.

## Responsibilities
- Calculate vertex size from FVF flags
- Determine offsets for vertex components (position, normal, diffuse, etc.)
- Provide human-readable FVF names for debugging

## Key Types
- **FVFInfoClass (Class)**: Manages FVF layout and component offsets
- **None (Enums)**: Uses D3D FVF flags directly

## Key Functions
### Get_FVF_Vertex_Size
- Purpose: Returns the size of a vertex in bytes based on FVF flags
- Calls: D3DXGetFVFVertexSize

### FVFInfoClass::Get_FVF_Name
- Purpose: Converts FVF flags to a human-readable string
- Calls: None

## Globals
- **None**

## Dependencies
- dx8fvf.h (header)
- wwstring.h (StringClass)
- D3dx8core.h (D3DXGetFVFVertexSize)
- DirectX 8 FVF flags (D3DFVF_*)
