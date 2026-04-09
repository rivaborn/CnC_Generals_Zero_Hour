# Generals/Code/Libraries/Source/WWVegas/WW3D2/shader.h

## Purpose
Defines the ShaderClass for managing rendering states in the SAGE engine, including blending, texturing, fog, and depth operations.

## Responsibilities
- Encapsulates rendering state configuration via bit flags
- Provides preset shaders for common rendering scenarios
- Supports alpha testing, fog, gradients, and blending modes
- Manages global backface culling state
- Converts material definitions into shader configurations

## Key Types
- ShaderClass (Class): Core shader state container with bitmask-based configuration
- ShaderShiftConstants (Enum): Bit shift positions for shader state flags
- AlphaTestType (Enum): Alpha testing modes (disable/enable)
- DepthCompareType (Enum): Depth comparison operations (never/less/equal/etc.)
- DepthMaskType (Enum): Depth buffer write control (disable/enable)
- ColorMaskType (Enum): Color buffer write control (disable/enable)
- DetailAlphaFuncType (Enum): Detail texture alpha blending modes
- DetailColorFuncType (Enum): Detail texture color blending modes
- CullModeType (Enum): Face culling modes (disable/enable)
- NPatchEnableType (Enum): NPatch surface support (disable/enable)
- DstBlendFuncType (Enum): Destination blend factors
- FogFuncType (Enum): Fog application modes
- PriGradientType (Enum): Primary gradient/texture blending modes
- SecGradientType (Enum): Secondary gradient control
- SrcBlendFuncType (Enum): Source blend factors
- TexturingType (Enum): Texturing enable/disable
- StaticSortCategoryType (Enum): Rendering sort categories

## Key Functions
### Apply
- Purpose: Applies the shader state to the rendering pipeline
- Calls: Not inferable

### Reset
- Purpose: Resets shader to default state
- Calls: Set_Depth_Compare, Set_Depth_Mask, etc.

### Uses_Alpha
- Purpose: Determines if shader uses alpha blending or testing
- Calls: Get_Alpha_Test, Get_Dst_Blend_Func, Get_Src_Blend_Func

### Uses_Fog
- Purpose: Checks if fog is enabled
- Calls: Get_Fog_Func

### Uses_Primary_Gradient
- Purpose: Checks if primary gradient is enabled
- Calls: Get_Primary_Gradient

### Uses_Secondary_Gradient
- Purpose: Checks if secondary gradient is enabled
- Calls: Get_Secondary_Gradient

### Uses_Texture
- Purpose: Checks if texturing is enabled
- Calls: Get_Texturing

### Uses_Post_Detail_Texture
- Purpose: Checks if post-detail texturing is used
- Calls: Get_Texturing
