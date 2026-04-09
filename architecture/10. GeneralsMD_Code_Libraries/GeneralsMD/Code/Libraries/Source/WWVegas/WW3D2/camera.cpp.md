# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/camera.cpp

## Purpose
Implements the CameraClass for 3D rendering, handling view transformations, projection, and frustum culling.

## Responsibilities
- Manages camera position, orientation, and projection parameters
- Handles point projection/unprojection between world and view space
- Updates frustum for visibility culling
- Provides device-to-world coordinate conversion
- Applies D3D rendering states

## Key Types
- **CameraClass (Class)**: Core camera implementation
- **ProjectionResType (Enum)**: Result of projection operations (INSIDE_FRUSTUM, OUTSIDE_FRUSTUM, OUTSIDE_NEAR_CLIP, OUTSIDE_FAR_CLIP)

## Key Functions
### Update_Frustum
- Purpose: Recalculates frustum planes and projection matrices
- Calls: Get_View_Plane, Get_Clip_Planes, Frustum.Init, ProjectionTransform.Init_Perspective/Init_Ortho

### Project
- Purpose: Projects world space points to view plane coordinates
- Calls: Update_Frustum, Matrix3D::Transform_Vector

### Un_Project
- Purpose: Converts view plane coordinates back to world space
- Calls: Matrix3D::Transform_Vector

### Apply
- Purpose: Sets D3D rendering states for this camera
- Calls: Update_Frustum, DX8Wrapper::Set_Viewport, DX8Wrapper::Set_Projection_Transform_With_Z_Bias

## Globals
None

## Dependencies
- camera.h (header)
- ww3d.h (WW3D engine)
- matrix4.h (matrix operations)
- dx8wrapper.h (D3D interface)
