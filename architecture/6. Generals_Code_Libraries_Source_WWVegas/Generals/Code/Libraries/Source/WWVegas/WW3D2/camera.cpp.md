# Generals/Code/Libraries/Source/WWVegas/WW3D2/camera.cpp

## Purpose
Implements the CameraClass for 3D rendering, handling view transformations, projection, and frustum culling.

## Responsibilities
- Manages camera position, orientation, and projection parameters
- Performs point/world space transformations
- Handles frustum culling and visibility tests
- Provides D3D state setup for rendering

## Key Types
- CameraClass (Class): Core camera implementation
- ProjectionResType (Enum): Projection result status (INSIDE_FRUSTUM, OUTSIDE_FRUSTUM, etc.)
- FrustumClass (External): Frustum representation for culling

## Key Functions
### Project
- Purpose: Projects world space points to view plane coordinates
- Calls: Update_Frustum, Matrix3D operations

### Un_Project
- Purpose: Converts view plane coordinates back to world space
- Calls: Matrix3D::Transform_Vector

### Update_Frustum
- Purpose: Recalculates frustum parameters when camera changes
- Calls: Frustum.Init, Matrix3D operations

### Apply
- Purpose: Sets D3D rendering states for this camera
- Calls: Update_Frustum, DX8Wrapper functions

### Cull_Box
- Purpose: Tests if an axis-aligned box is outside the frustum
- Calls: Get_Frustum, CollisionMath::Overlap_Test

## Globals
- None

## Dependencies
- camera.h (header)
- ww3d.h (engine interface)
- matrix4.h (matrix operations)
- dx8wrapper.h (D3D abstraction)
