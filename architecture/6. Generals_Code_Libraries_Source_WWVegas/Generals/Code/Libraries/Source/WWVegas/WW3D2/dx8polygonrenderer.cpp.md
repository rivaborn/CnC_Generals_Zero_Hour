# Generals/Code/Libraries/Source/WWVegas/WW3D2/dx8polygonrenderer.cpp

## Purpose
Implements the DX8PolygonRendererClass for managing polygon rendering in the DirectX 8 renderer.

## Responsibilities
- Manages polygon rendering state for mesh models
- Handles vertex and index buffer offsets
- Tracks texture categories and rendering passes
- Mainages lifecycle in a linked list via MeshModelClass

## Key Types
- DX8PolygonRendererClass (Class): Manages polygon rendering parameters for a mesh model

## Key Functions
### DX8PolygonRendererClass constructor
- Purpose: Initializes polygon renderer with index count, mesh model, texture category, and offsets
- Calls: `mmc->PolygonRendererList.Add_Tail(this)`

### DX8PolygonRendererClass copy constructor
- Purpose: Creates a copy of a polygon renderer for a different mesh model
- Calls: `mmc->PolygonRendererList.Add_Tail(this)`

### ~DX8PolygonRendererClass destructor
- Purpose: Cleans up polygon renderer and notifies texture category
- Calls: `texture_category->Remove_Polygon_Renderer(this)`

### Log
- Purpose: Outputs diagnostic information about the polygon renderer
- Calls: `WWDEBUG_SAY`

## Globals
- None

## Dependencies
- `dx8polygonrenderer.h`
- `dx8renderer.h`
- `MeshModelClass`
- `DX8TextureCategoryClass`
- `StringClass`
- `WWDEBUG_SAY`
- `WWASSERT`
