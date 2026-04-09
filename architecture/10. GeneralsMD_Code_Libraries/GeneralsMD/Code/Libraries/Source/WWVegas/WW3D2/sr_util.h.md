# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/sr_util.h

## Purpose
Header file providing utility functions and classes for converting between Westwood (W3D) and Surrender (SR) rendering coordinate systems and data structures.

## Responsibilities
- Matrix and vector type conversions between W3D and SR systems
- Camera frustum corner calculations
- Reference counting macros for SR objects
- SRMeshClass for mesh intersection testing data

## Key Types
- **srNode (Class)**: Surrender node object (forward declaration)
- **srMeshModel (Class)**: Surrender mesh model (forward declaration)
- **srCamera (Class)**: Surrender camera (forward declaration)
- **srGERD (Class)**: Surrender rendering device (forward declaration)
- **CameraClass (Class)**: W3D camera class (forward declaration)
- **RenderObjClass (Class)**: W3D render object (forward declaration)
- **POLYGONINDEX (Class)**: Typedef for unsigned short polygon index
- **SRMeshClass (Class)**: Stores mesh data for intersection testing

## Key Functions
### Set_SR_Transform
- Purpose: Sets transform for a surrender node from W3D matrix
- Calls: Not inferable

### Get_SR_Transform
- Purpose: Gets W3D matrix from surrender node transform
- Calls: Not inferable

### Set_SR_Camera_Transform
- Purpose: Sets transform for a surrender camera from W3D matrix
- Calls: Not inferable

### Get_SR_Camera_Transform
- Purpose: Gets W3D matrix from surrender camera transform
- Calls: Not inferable

### Push_Multiply_Westwood_Matrix
- Purpose: Push-multiplies a W3D matrix into a surrender GERD
- Calls: Convert_Westwood_Matrix

### Convert_Westwood_Matrix (variants)
- Purpose: Converts between W3D and surrender matrix/vector types
- Calls: Not inferable

### Convert_Surrender_Matrix (variants)
- Purpose: Converts surrender matrices back to W3D format
- Calls: Not inferable

### Multiply_Westwood_And_Surrender_Matrix
- Purpose: Multiplies W3D and surrender matrices
- Calls: Not inferable

### As_Vector3/As_srVector3 (variants)
- Purpose: Type-casting between W3D and surrender vector types
- Calls: Not inferable

### Get_Camera_Frustum_Corners
- Purpose: Calculates world-space frustum corners for a camera
- Calls: Not inferable

### Get_ZClamped_Camera_Frustum_Corners
- Purpose: Calculates frustum corners with depth clamping
