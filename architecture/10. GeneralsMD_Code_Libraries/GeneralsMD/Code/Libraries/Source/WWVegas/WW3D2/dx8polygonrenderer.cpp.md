# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/dx8polygonrenderer.cpp

## Purpose
Implements the DX8PolygonRendererClass, managing polygon rendering for DirectX 8 in the SAGE engine.

## Responsibilities
- Manages polygon rendering state for mesh models
- Handles vertex/index buffer offsets and ranges
- Maintains texture category associations
- Supports polygon strip rendering
- Integrates with the mesh model's renderer list

## Key Types
- **DX8PolygonRendererClass (Class)**: Manages polygon rendering parameters for a mesh model
- **MeshModelClass (Pointer)**: Reference to the owning mesh model
- **DX8TextureCategoryClass (Pointer)**: Reference to the texture category

## Key Functions
### DX8PolygonRendererClass (Constructor)
- Purpose: Initializes polygon renderer with index count, mesh model, texture category, and offsets
- Calls: `mmc->PolygonRendererList.Add_Tail(this)`

### DX8PolygonRendererClass (Copy Constructor)
- Purpose: Creates a copy of a polygon renderer for a different mesh model
- Calls: `mmc->PolygonRendererList.Add_Tail(this)`

### ~DX8PolygonRendererClass (Destructor)
- Purpose: Cleans up polygon renderer and notifies texture category
- Calls: `texture_category->Remove_Polygon_Renderer(this)`

### Log
- Purpose: Outputs debug information about the polygon renderer
- Calls: `WWDEBUG_SAY`

## Globals
None

## Dependencies
- `dx8polygonrenderer.h`
- `dx8renderer.h`
- `StringClass`
- `WWDEBUG_SAY`
- `WWASSERT`
