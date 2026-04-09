# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/camera.h

## Purpose
Defines camera-related classes for 3D rendering, including viewport management, projection handling, and frustum culling.

## Responsibilities
- Manages camera transformations and projections (perspective/orthographic)
- Handles viewport and clipping plane configuration
- Provides frustum-based culling for rendering optimization
- Supports point projection/unprojection between coordinate spaces

## Key Types
- **ViewportClass (Class)**: Defines normalized screen space rectangle for rendering
- **CameraClass (Class)**: Core camera class handling view transformations and projections
- **ProjectionType (Enum)**: Type of projection (perspective/orthographic)
- **ProjectionResType (Enum)**: Result types for projection operations

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

### `Cull_Sphere`
- Purpose: Tests if sphere is outside view frustum
- Calls: `Get_Frustum()`, `CollisionMath::Overlap_Test`

## Globals
None

## Dependencies
- `rendobj.h`, `plane.h`, `frustum.h`, `obbox.h`, `vector2.h`, `matrix4.h`, `colmath.h`
- `RenderInfoClass` (forward declaration)
- `CollisionMath` namespace for overlap tests
