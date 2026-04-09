# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/linegrp.cpp

## Purpose
Manages rendering of line groups (tetrahedrons/prisms) aligned with the view plane for visual effects.

## Responsibilities
- Handles line group geometry construction and rendering
- Manages vertex/index buffers for line primitives
- Configures shaders and materials for line rendering
- Supports per-line attributes (color, size, UV coords)
- Implements sorting for translucent lines

## Key Types
- **LineGroupClass (Class)**: Main line group manager
- **LineModeType (Enum)**: Line rendering mode (TETRAHEDRON/PRISM)
- **FlagsType (Enum)**: Rendering flags (TRANSFORM)

## Key Functions
### `Set_Arrays`
- Purpose: Assigns input arrays for line positions/attributes
- Calls: `REF_PTR_SET`, `WWASSERT`

### `Render`
- Purpose: Renders all lines in the group
- Calls: `DX8Wrapper::Set_Transform`, `DX8Wrapper::Set_Shader`, `SortingRendererClass::Insert_Triangles`, etc.

### `Get_Polygon_Count`
- Purpose: Returns total polygon count for all lines
- Calls: None

## Globals
- **None**

## Dependencies
- `sharebuf.h`, `linegrp.h`, `texture.h`, `vertmaterial.h`, `dx8wrapper.h`, `wwmath.h`, `rinfo.h`, `camera.h`, `dx8indexbuffer.h`, `dx8vertexbuffer.h`, `sortingrenderer.h`
- `DX8Wrapper`, `ShaderClass`, `TextureClass`, `VertexMaterialClass`, `SortingRendererClass`
