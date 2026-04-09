# Generals/Code/Libraries/Source/WWVegas/WW3D2/dx8fvf.h

## Purpose
Defines vertex format structures and FVF (Flexible Vertex Format) handling for Direct3D 8 rendering.

## Responsibilities
- Declares vertex format structs for various attribute combinations
- Defines FVF flags as enums
- Provides FVFInfoClass to query vertex buffer layout information
- Supports memory pooling for FVFInfoClass instances

## Key Types
- StringClass (Class): Not inferable (forward declaration)
- (anonymous enum) (Enum): D3D8 FVF flag combinations
- DX8_FVF_XYZ (Enum): FVF flag for position-only vertices
- DX8_FVF_XYZN (Enum): FVF flag for position+normal vertices
- DX8_FVF_XYZNUV1 (Enum): FVF flag for position+normal+texcoord1
- DX8_FVF_XYZNUV2 (Enum): FVF flag for position+normal+texcoord2
- DX8_FVF_XYZNDUV1 (Enum): FVF flag for position+normal+diffuse+texcoord1
- DX8_FVF_XYZNDUV2 (Enum): FVF flag for position+normal+diffuse+texcoord2
- DX8_FVF_XYZDUV1 (Enum): FVF flag for position+diffuse+texcoord1
- DX8_FVF_XYZDUV2 (Enum): FVF flag for position+diffuse+texcoord2
- DX8_FVF_XYZUV1 (Enum): FVF flag for position+texcoord1
- DX8_FVF_XYZUV2 (Enum): FVF flag for position+texcoord2
- VertexFormatXYZ (Class): Vertex struct with position only
- VertexFormatXYZNUV1 (Class): Vertex struct with position, normal, and 1 texcoord
- VertexFormatXYZNUV2 (Class): Vertex struct with position, normal, and 2 texcoords
- VertexFormatXYZN (Class): Vertex struct with position and normal
- VertexFormatXYZNDUV1 (Class): Vertex struct with position, normal, diffuse, and 1 texcoord
- VertexFormatXYZNDUV2 (Class): Vertex struct with position, normal, diffuse, and 2 texcoords
- VertexFormatXYZDUV1 (Class): Vertex struct with position, diffuse, and 1 texcoord
- VertexFormatXYZDUV2 (Class): Vertex struct with position, diffuse, and 2 texcoords
- VertexFormatXYZUV1 (Class): Vertex struct with position and 1 texcoord
- VertexFormatXYZUV2 (Class): Vertex struct with position and 2 texcoords
