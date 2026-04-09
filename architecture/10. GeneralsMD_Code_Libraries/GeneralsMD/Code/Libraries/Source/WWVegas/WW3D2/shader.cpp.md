# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/shader.cpp

## Purpose
Manages shader states and rendering configurations for the W3D rendering engine, including preset shaders and Direct3D state application.

## Responsibilities
- Defines preset shader configurations for various rendering scenarios
- Applies shader states to the Direct3D device
- Manages backface culling inversion
- Provides helper functions for static sorting and shader categorization
- Initializes shaders from material definitions

## Key Types
- **Blend (Class)**: Wraps D3DBLEND enum with alpha usage flag
- **ShaderClass (Class)**: Main shader management class (defined elsewhere)
- **StaticSortCategoryType (Enum)**: Categories for static sorting (SSCAT_OPAQUE, SSCAT_ALPHA_TEST, SSCAT_ADDITIVE, SSCAT_SCREEN, SSCAT_OTHER)

## Key Functions
### ShaderClass::Init_From_Material3
- Purpose: Initialize shader from Material3 structure
- Calls: Set_Depth_Mask, Set_Dst_Blend_Func, Set_Src_Blend_Func

### ShaderClass::Enable_Fog
- Purpose: Enable appropriate fog mode based on blend functions
- Calls: Get_Src_Blend_Func, Get_Dst_Blend_Func, Set_Fog_Func, Report_Unable_To_Fog

### ShaderClass::Apply
- Purpose: Apply all render states for this shader
- Calls: DX8Wrapper methods, SetTextureStageState, SetTexture

### ShaderClass::Invert_Backface_Culling
- Purpose: Globally invert backface culling mode
- Calls: None

### ShaderClass::Get_SS_Category
- Purpose: Determine static sort category based on shader properties
- Calls: Get_Alpha_Test, Get_Dst_Blend_Func, Get_Src_Blend_Func

### ShaderClass::Guess_Sort_Level
- Purpose: Guess appropriate sort level based on shader category
- Calls: Get_SS_Category

### ShaderClass::Is_Backface_Culling_Inverted
- Purpose: Check if backface culling is inverted
- Calls: None

## Globals
- **ShaderDirty (bool)**: Tracks if shader states need updating
- **CurrentShader (unsigned long)**: Currently active shader ID
- **_PolygonCullMode (unsigned long)**: Current polygon culling mode
- **srcBlendLUT (Blend[])**: Lookup table for source blend modes
- **dstBlendLUT (Blend[])**: Lookup table for destination blend modes
- **_Preset*Shader (ShaderClass)**: Various preset shader instances

## Dependencies
- shader.h, w3d_file.h, wwdebug.h, Dx8Wrapper.h, dx8caps.h
- Direct3D 8/9 API (D3D* types)
- WW3D namespace functions (Get_NPatches_Level, Is_Coloring_Enabled)
