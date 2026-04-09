# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/w3d_util.cpp

## Purpose
Provides utility functions for converting between W3D engine data structures and internal game math types.

## Responsibilities
- Convert vectors, quaternions, and colors between W3D and internal formats
- Convert shader settings between W3D and internal shader classes
- Handle type conversions for 3D math and rendering pipelines

## Key Types
- W3dUtilityClass (Class): utility methods for type conversions
- W3dVectorStruct (Struct): W3D vector type
- Vector3 (Struct): internal vector type
- W3dQuaternionStruct (Struct): W3D quaternion type
- Quaternion (Struct): internal quaternion type
- W3dRGBStruct (Struct): W3D RGB color type
- W3dRGBAStruct (Struct): W3D RGBA color type
- Vector4 (Struct): internal 4D vector type
- W3dShaderStruct (Struct): W3D shader type
- ShaderClass (Class): internal shader class

## Key Functions
### Convert_Vector
- Purpose: Convert between W3D vector and internal Vector3
- Calls: None

### Convert_Quaternion
- Purpose: Convert between W3D quaternion and internal Quaternion
- Calls: None

### Convert_Color
- Purpose: Convert between W3D color types and internal vector types
- Calls: None

### Convert_Shader
- Purpose: Convert between W3D shader and internal ShaderClass
- Calls: W3d_Shader_Get_* and W3d_Shader_Set_* functions

## Globals
- None

## Dependencies
- w3d_util.h
- vector3.h
- vector4.h
- quat.h
- shader
