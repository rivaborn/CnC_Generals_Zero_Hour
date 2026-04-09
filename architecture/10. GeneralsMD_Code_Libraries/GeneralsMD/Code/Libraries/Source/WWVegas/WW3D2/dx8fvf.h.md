# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/dx8fvf.h

## Purpose
Defines vertex format structures and FVF (Flexible Vertex Format) handling for Direct3D 8 rendering in the SAGE engine.

## Responsibilities
- Declares vertex format enums and structs for various vertex buffer layouts
- Provides FVFInfoClass for querying vertex buffer element offsets
- Supports Direct3D 8 vertex shader compatibility

## Key Types
- StringClass (Class): Not inferable (forward declaration)
- (anonymous enum): Contains DX8_FVF_* vertex format flags
- DX8_FVF_XYZ (Enum): Flag for position-only vertex format
- DX8_FVF_XYZN (Enum): Flag for position+normal vertex format
- DX8_FVF_XYZNUV1 (Enum): Flag for position+normal+1 texture coord
- DX8_FVF_XYZNUV2 (Enum): Flag for position+normal+2 texture coords
- DX8_FVF_XYZNDUV1 (Enum): Flag for position+normal+diffuse+1 texture coord
- DX8_FVF_XYZNDUV2 (Enum): Flag for position+normal+diffuse+2 texture coords
- DX8_FVF_XYZDUV1 (Enum): Flag for position+diffuse+1 texture coord
- DX8_FVF_XYZDUV2 (Enum): Flag for position+diffuse+2 texture coords
- DX8_FVF_XYZUV1 (Enum): Flag for position+1 texture coord
- DX8_FVF_XYZUV2 (Enum): Flag for position+2 texture coords
- DX8_FVF_XYZNDUV1TG3 (Enum): Flag for tangent-space lighting format
- DX8_FVF_XYZNUV2DMAP (Enum): Flag for displacement mapping format
- DX8_FVF_XYZNDCUBEMAP (Enum): Flag for cube mapping format
- VertexFormatXYZ (Class): Position-only vertex structure
- VertexFormatXYZNUV1 (Class): Position+normal+1 texture coord structure
- VertexFormatXYZNUV2 (Class): Position+normal+2 texture coords structure
- VertexFormatXYZN (Class): Position+normal structure
- VertexFormatXYZNDUV1 (Class): Position+normal+diffuse+1 texture coord
- VertexFormatXYZNDUV2 (Class): Position+normal+diffuse+2 texture coords
- VertexFormatXYZDUV1 (Class): Position+diffuse+1 texture coord
- VertexFormatXYZDUV2 (Class): Position+diffuse+2 texture coords
- VertexFormatXYZUV1 (Class): Position+1 texture coord
- VertexFormatXYZUV
