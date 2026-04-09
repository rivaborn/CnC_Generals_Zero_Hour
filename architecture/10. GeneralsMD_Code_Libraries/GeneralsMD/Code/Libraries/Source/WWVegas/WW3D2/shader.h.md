# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/shader.h

## Purpose
Defines the ShaderClass and related enums for rendering state management in the SAGE engine.

## Responsibilities
- Encapsulates rendering state (blending, texturing, fog, etc.) as bit flags
- Provides getter/setter methods for shader properties
- Manages predefined shader presets for common rendering cases
- Handles DirectX 8 state management via DX8Wrapper

## Key Types
- **ShaderClass (Class)**: Core class managing rendering shader state
- **ShaderShiftConstants (Enum)**: Bit shift positions for shader flags
- **AlphaTestType (Enum)**: Alpha testing modes
- **DepthCompareType (Enum)**: Depth comparison functions
- **DepthMaskType (Enum)**: Depth buffer write modes
- **ColorMaskType (Enum)**: Color buffer write modes
- **DetailAlphaFuncType (Enum)**: Detail texture alpha functions
- **DetailColorFuncType (Enum)**: Detail texture color functions
- **CullModeType (Enum)**: Face culling modes
- **NPatchEnableType (Enum)**: NPatch surface enabling
- **DstBlendFuncType (Enum)**: Destination blend functions
- **FogFuncType (Enum)**: Fog application modes
- **PriGradientType (Enum)**: Primary gradient modes
- **SecGradientType (Enum)**: Secondary gradient modes
- **SrcBlendFuncType (Enum)**: Source blend functions
- **TexturingType (Enum)**: Texturing enable/disable
- **StaticSortCategoryType (Enum)**: Sorting categories for transparency

## Key Functions
### Reset
- Purpose: Resets shader to default state
- Calls: None

### Get_SS_Category
- Purpose: Returns static sort category based on shader settings
- Calls: None

### Guess_Sort_Level
- Purpose: Estimates sort level for transparency rendering
- Calls: None

### Invert_Backface_Culling
- Purpose: Globally inverts backface culling
- Calls: None

### Is_Backface_Culling_Inverted
- Purpose: Checks if backface culling is inverted
- Calls: None

### Get_Description
- Purpose: Generates human-readable description of shader
- Calls: None

## Globals
- **ShaderDirty (bool)**: Tracks if shader state needs updating
- **CurrentShader (unsigned long)**: Currently active shader
- **_PresetOpaqueShader (ShaderClass)**: Predefined opaque shader
- **_PresetAdditiveShader (ShaderClass)**: Predefined additive shader
- **_PresetBumpenvmapShader (ShaderClass)**: Predefined bump envmap shader
- **_PresetAlphaShader (ShaderClass)**: Predefined alpha shader
- **_Pres
