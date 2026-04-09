# Generals/Code/Libraries/Source/WWVegas/WW3D2/w3d_util.h

## Purpose
Header file defining utility functions for converting between W3D file-format structures and runtime classes.

## Responsibilities
- Provides conversion utilities between W3D file structures and runtime classes
- Handles Vector3, Vector4, Quaternion, and Shader conversions
- Supports color conversions in RGB and RGBA formats

## Key Types
- Vector3 (Class): 3D vector representation
- Vector4 (Class): 4D vector representation
- Quaternion (Class): Quaternion rotation representation
- ShaderClass (Class): Shader representation
- W3dUtilityClass (Class): Utility class containing conversion methods

## Key Functions
### Convert_Vector
- Purpose: Converts between W3dVectorStruct and Vector3
- Calls: None

### Convert_Quaternion
- Purpose: Converts between W3dQuaternionStruct and Quaternion
- Calls: None

### Convert_Color
- Purpose: Converts between W3dRGBStruct/W3dRGBAStruct and Vector3/Vector4
- Calls: None

### Convert_Shader
- Purpose: Converts between W3dShaderStruct and ShaderClass
- Calls: None

## Globals
None

## Dependencies
- "always.h"
- "w3d_file.h"
- Vector3, Vector4, Quaternion, ShaderClass (forward declarations)
