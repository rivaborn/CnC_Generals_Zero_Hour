# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/sr_util.cpp

## Purpose
Provides utility functions for converting between Westwood 3D (W3D) and Surrender (SR) matrix/transform formats, and for calculating camera frustum corners.

## Responsibilities
- Convert between W3D and SR matrix formats
- Set/get transforms for SR nodes and cameras
- Calculate camera frustum corners (with optional Z-clamping)

## Key Types
None

## Key Functions
### Set_SR_Transform
- Purpose: Copies a W3D transform into a SR node
- Calls: srNode::setLocation, srNode::setRotation

### Get_SR_Transform
- Purpose: Creates a W3D Matrix3D from a SR node transform
- Calls: srNode::getLocation, srNode::getRotation

### Set_SR_Camera_Transform
- Purpose: Copies a W3D transform into a SR camera
- Calls: srCamera::setLocation, srCamera::setRotation

### Get_SR_Camera_Transform
- Purpose: Creates a W3D Matrix3D from a SR camera transform
- Calls: srCamera::getLocationX/Y/Z, srCamera::getRotation

### Push_Multiply_Westwood_Matrix
- Purpose: Pushes and multiplies a W3D matrix into the SR GERD
- Calls: srGERD::matrixMode, srGERD::pushMultMatrix, Convert_Westwood_Matrix

### Get_Camera_Frustum_Corners
- Purpose: Returns 8 camera frustum corner points in world space
- Calls: CameraClass::Get_View_Plane, CameraClass::Get_Clip_Planes, CameraClass::Get_Transform, Matrix3D::Transform_Vector

### Get_ZClamped_Camera_Frustum_Corners
- Purpose: Returns Z-clamped camera frustum corners
- Calls: CameraClass::Get_View_Plane, CameraClass::Get_Clip_Planes, CameraClass::Get_Transform, Matrix3D::Transform_Vector

## Globals
None

## Dependencies
- srNode.hpp, srCamera.hpp, srMeshModel.hpp, srGERD.hpp (Surrender SDK)
- wwdebug.h (Westwood debug utilities)
- camera.h (W3D camera class)
- matrix4.h (W3D matrix classes)
