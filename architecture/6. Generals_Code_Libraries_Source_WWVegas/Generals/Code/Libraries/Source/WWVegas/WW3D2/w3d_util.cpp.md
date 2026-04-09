# Generals/Code/Libraries/Source/WWVegas/WW3D2/w3d_util.cpp

## Purpose
Provides utility functions for converting between W3D engine data structures and internal game math types.

## Responsibilities
- Convert vectors, quaternions, and colors between W3D and game engine formats
- Convert shader settings between W3D and game engine formats
- Handle type conversions for rendering pipeline compatibility

## Key Types
- W3dUtilityClass (Class): utility methods for type conversions
- W3dVectorStruct (Struct): W3D vector type
- Vector3 (Struct): game engine vector type
- W3dQuaternionStruct (Struct): W3D quaternion type
- Quaternion (Struct): game engine quaternion type
- W3dRGBStruct (Struct): W3D RGB color type
- Vector4 (Struct): game engine 4D vector type
- W3dRGBAStruct (Struct): W3D RGBA color type
- W3dShaderStruct (Struct): W3D shader configuration
- ShaderClass (Class): game engine shader class

## Key Functions
### Convert_Vector
- Purpose: Convert between W3D vector and Vector3 types
- Calls: None

### Convert_Quaternion
- Purpose: Convert between W3D quaternion and Quaternion types
- Calls: None

### Convert_Color
- Purpose: Convert between W3D color types and Vector3/Vector4 types
- Calls: None

### Convert_Shader
- Purpose: Convert shader settings between W3D and ShaderClass types
- Calls: W3d_Shader_Get_* and W3d_Shader_Set_* functions

## Globals
- None

## Dependencies
- w3d_util.h
- vector3.h
- vector4.h
- quat
