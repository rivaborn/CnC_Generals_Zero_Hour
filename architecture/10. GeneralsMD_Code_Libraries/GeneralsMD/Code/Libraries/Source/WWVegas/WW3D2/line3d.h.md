# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/line3d.h

## Purpose
Defines the `Line3DClass` for rendering 3D line segments in the W3D rendering system.

## Responsibilities
- Render 3D line segments as cylinders with configurable width.
- Manage line properties (position, color, opacity, sorting).
- Provide bounding volume queries for collision/visibility.

## Key Types
- **Line3DClass (Class)**: Renders 3D line segments with configurable width and color.
- **VertexMaterialClass (Class)**: Forward declaration (material handling).
- **RenderInfoClass (Class)**: Forward declaration (rendering context).

## Key Functions
### `Line3DClass(const Vector3 & start, const Vector3 & end, float width, float r, float g, float b, float opacity)`
- Purpose: Constructs a 3D line segment.
- Calls: Not inferable.

### `Render(RenderInfoClass & rfinfo)`
- Purpose: Renders the line segment.
- Calls: Not inferable.

### `Reset(const Vector3 & new_start, const Vector3 & new_end)`
- Purpose: Updates line endpoints.
- Calls: Not inferable.

### `Re_Color(float r, float g, float b)`
- Purpose: Changes line color.
- Calls: Not inferable.

## Globals
- None.

## Dependencies
- `rendobj.h` (base class `RenderObjClass`)
- `vector3.h`, `vector4.h` (math types)
- `shader.h` (shader handling)
- `always.h` (common includes)
