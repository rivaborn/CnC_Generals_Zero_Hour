# Generals/Code/Libraries/Source/WWVegas/WW3D2/sr_util.h

## Purpose
Header file providing utility functions and type conversions between Westwood's W3D engine and the Surrender (SR) rendering system.

## Responsibilities
- Matrix and vector type conversions between W3D and SR systems
- Camera frustum corner calculations
- Reference counting macros for SR objects
- SRMeshClass for mesh intersection testing

## Key Types
- **srNode (Class)**: Surrender node object
- **srMeshModel (Class)**: Surrender mesh model
- **srCamera (Class)**: Surrender camera
- **srGERD (Class)**: Surrender rendering device
- **CameraClass (Class)**: W3D camera class
- **RenderObjClass (Class)**: W3D render object
- **POLYGONINDEX (Class)**: Typedef for unsigned short
- **SRMeshClass (Class)**: Stores mesh data for intersection testing

## Key Functions
### Set_SR_Transform
- Purpose: Sets transform for SR node from W3D matrix
- Calls: Not inferable

### Get_SR_Transform
- Purpose: Gets transform from SR node as W3D matrix
- Calls: Not inferable

### Set_SR_Camera_Transform
- Purpose: Sets transform for SR camera from W3D matrix
- Calls: Not inferable

### Get_SR_Camera_Transform
- Purpose: Gets transform from SR camera as W3D matrix
- Calls: Not inferable

### Push_Multiply_Westwood_Matrix
- Purpose: Push-multiplies W3D matrix into SR GERD
- Calls: Convert_Westwood_Matrix

### Convert_Westwood_Matrix
- Purpose: Converts between W3D and SR matrix types
- Calls: Not inferable

### Convert_Surrender_Matrix
- Purpose: Converts SR matrix to W3D matrix
- Calls: Not inferable

### Multiply_Westwood_And_Surrender_Matrix
- Purpose: Multiplies W3D and SR matrices
- Calls: Not inferable

### Get_Camera_Frustum_Corners
- Purpose: Gets worldspace frustum corners for camera
- Calls: Not inferable

### Get_ZClamped_Camera_Frustum_Corners
- Purpose: Gets frustum corners with Z clamping
- Calls: Not inferable

## Globals
- **As_Vector3 (function)**: Casts between Vector3 and srVector3

## Dependencies
- "matrix3d.h", "vector3i.h"
- srVector3i.hpp, srVector3.hpp, srVector2.hpp, srMatrix4x3.hpp
- srNode, sr
