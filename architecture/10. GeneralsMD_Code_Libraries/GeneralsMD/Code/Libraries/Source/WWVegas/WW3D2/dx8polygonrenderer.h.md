# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/dx8polygonrenderer.h

## Purpose
Defines the DX8PolygonRendererClass for managing and rendering batches of polygons using DirectX 8.

## Responsibilities
- Stores polygon batch data (indices, vertices, texture category)
- Provides rendering methods (strips, triangles, sorted)
- Manages vertex/index offsets and rendering passes
- Integrates with DX8Wrapper for actual rendering calls

## Key Types
- **DX8PolygonRendererClass (Class)**: Represents a batch of polygons to render.
- **DX8TextureCategoryClass (Class)**: Texture category reference (forward declared).
- **None**: No enums/structs defined.

## Key Functions
### DX8PolygonRendererClass::Render
- Purpose: Renders polygon batch (strip or triangles).
- Calls: DX8Wrapper::Set_Index_Buffer_Index_Offset, DX8Wrapper::Draw_Strip/Draw_Triangles

### DX8PolygonRendererClass::Render_Sorted
- Purpose: Inserts triangles into sorting renderer for depth-sorted rendering.
- Calls: DX8Wrapper::Set_Index_Buffer_Index_Offset, SortingRendererClass::Insert_Triangles

### DX8PolygonRendererClass::Set_Vertex_Index_Range
- Purpose: Sets the vertex index range for the polygon batch.
- Calls: None

## Globals
- None

## Dependencies
- Key includes: "always.h", "meshmdl.h", "dx8list.h", "sortingrenderer.h", "mesh.h", "dx8wrapper.h"
- External symbols: MultiListObjectClass, MeshModelClass, DX8Wrapper, SortingRendererClass, SphereClass, Matrix3D
