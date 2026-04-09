# Generals/Code/Libraries/Source/WWVegas/WW3D2/sr_util.cpp

## Purpose
Provides utility functions for converting between Westwood 3D (W3D) and Surrender (SR) matrix/transform formats, and for calculating camera frustum corners.

## Responsibilities
- Convert between W3D and Surrender matrix formats
- Set/get transforms for Surrender objects and cameras
- Calculate camera frustum corners in world space
- Handle z-clamped frustum corner calculations

## Key Types
None

## Key Functions
### Set_SR_Transform
- Purpose: Copies a W3D transform into a Surrender object
- Calls: obj->setLocation, obj->setRotation

### Get_SR_Transform
- Purpose: Creates a W3D Matrix3D from a Surrender object transform
- Calls: obj->getLocation, obj->getRotation

### Set_SR_Camera_Transform
- Purpose: Copies a W3D transform into a Surrender camera
- Calls: obj->setLocation, obj->setRotation

### Get_SR_Camera_Transform
- Purpose: Creates a W3D Matrix3D from a Surrender camera transform
- Calls: obj->getLocationX/Y/Z, obj->getRotation

### Push_Multiply_Westwood_Matrix
- Purpose: Pushes and multiplies a W3D matrix into the Surrender GERD
- Calls: gerd->matrixMode, Convert_Westwood_Matrix, gerd->pushMultMatrix

### Get_Camera_Frustum_Corners
- Purpose: Returns 8 camera frustum corner points in world space
- Calls: camera->Get_View_Plane, camera->Get_Clip_Planes, Matrix3D::Transform_Vector

### Get_ZClamped_Camera_Frustum_Corners
- Purpose: Gets z-clamped frustum corners with range checking
- Calls: camera->Get_View_Plane, camera->Get_Clip_Planes, Matrix3D::Transform_Vector

## Globals
None

## Dependencies
- sr_util.h, wwdebug.h, camera.h, matrix4.h
- Surrender headers: srNode.hpp, srCamera.hpp, srMeshModel.hpp, srGERD.hpp
- External symbols: Matrix3D, Vector3, Vector2, CameraClass
