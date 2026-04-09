# Generals/Code/Libraries/Source/WWVegas/WW3D2/camera.h

## Purpose
Defines camera-related classes for the WW3D rendering engine, including viewport management and projection handling.

## Responsibilities
- Manages camera projection (perspective/orthographic)
- Handles viewport and clipping plane configuration
- Provides frustum culling and point projection
- Maintains view-space transformations
- Exposes camera matrices for rendering

## Key Types
- **ViewportClass (Class)**: Defines normalized screen space rectangle for rendering
- **CameraClass (Class)**: Core camera class handling transformations and projections
- **ProjectionType (Enum)**: Perspective or orthographic projection modes
- **ProjectionResType (Enum)**: Result types for point projection (inside/outside frustum/clipping)

## Key Functions
### `Set_Transform`
- Purpose: Updates camera transform and invalidates frustum cache
- Calls: None (inline)

### `Project`
- Purpose: Projects world-space point into camera space
- Calls: None (inline)

### `Update_Frustum`
- Purpose: Recalculates frustum planes and corners
- Calls: None (inline)

### `Apply`
- Purpose: Applies camera settings to Direct3D
- Calls: None (implementation not shown)

## Globals
- None

## Dependencies
- `rendobj.h`, `plane.h`, `frustum.h`, `obbox.h`, `vector2.h`, `matrix4.h`, `colmath.h`
- `RenderInfoClass` (forward declaration)
- `CollisionMath` namespace for overlap tests
