# Generals/Code/Libraries/Source/WWVegas/WW3D2/shader.cpp

## Purpose
Manages shader states and rendering parameters for the SAGE engine's Direct3D 8 rendering pipeline.

## Responsibilities
- Defines preset shaders for common rendering scenarios (opaque, additive, alpha-blended, etc.)
- Applies shader states to the Direct3D device via DX8Wrapper
- Handles fog, blending, texturing, and culling modes
- Provides utility functions for static sorting and backface culling

## Key Types
- **Blend (Class)**: Maps shader blend modes to D3D blend functions
- **ShaderClass (Class)**: Core shader management class (defined in header)

## Key Functions
### `ShaderClass::Apply`
- Purpose: Applies all shader states to the Direct3D device
- Calls: `DX8Wrapper::Set_DX8_Texture_Stage_State`, `DX8Wrapper::Set_DX8_Render_State`

### `ShaderClass::Enable_Fog`
- Purpose: Configures fog based on current blend modes
- Calls: `Report_Unable_To_Fog`

### `ShaderClass::Invert_Backface_Culling`
- Purpose: Globally inverts backface culling direction
- Calls: None

### `ShaderClass::Get_SS_Category`
- Purpose: Determines static sort category for transparency handling
- Calls: None

### `ShaderClass::Guess_Sort_Level`
- Purpose: Guesses sort level based on blend modes
- Calls: `Get_SS_Category`

## Globals
- `_PolygonCullMode (unsigned long)`: Tracks current culling mode
- `srcBlendLUT (Blend[])`: Lookup table for source blend modes
- `dstBlendLUT (Blend[])`: Lookup table for destination blend modes

## Dependencies
- `shader.h`, `w3d_file.h`, `wwdebug.h`, `Dx8Wrapper.h`, `dx8caps.h`
- Direct3D 8 constants and types (D3DTEXTUREOP, D3DBLEND, etc.)
