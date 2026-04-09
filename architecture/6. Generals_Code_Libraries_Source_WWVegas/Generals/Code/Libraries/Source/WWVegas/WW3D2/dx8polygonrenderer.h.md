# Generals/Code/Libraries/Source/WWVegas/WW3D2/dx8polygonrenderer.h

## Purpose
Defines a DirectX 8 polygon renderer class for managing and rendering batches of polygons in the SAGE engine.

## Responsibilities
- Manages polygon batches with vertex/index buffers
- Handles rendering via DirectX 8 wrapper
- Supports both strip and triangle rendering
- Provides sorted rendering for transparency effects
- Tracks texture categories and mesh models

## Key Types
- **DX8PolygonRendererClass (Class)**: Represents a batch of polygons to render with vertex/index data
- **DX8TextureCategoryClass (Class)**: Texture category reference (forward declared)
- **None**: No enums/structs defined

## Key Functions
### DX8PolygonRendererClass::Render
- Purpose: Renders polygon batch using DirectX 8 wrapper
- Calls: DX8Wrapper::Set_Index_Buffer_Index_Offset, DX8Wrapper::Draw_Strip/Draw_Triangles

### DX8PolygonRendererClass::Render_Sorted
- Purpose: Renders polygons with sorting for transparency
- Calls: DX8Wrapper::Set_Index_Buffer_Index_Offset, SortingRendererClass::Insert_Triangles

### DX8PolygonRendererClass::Set_Vertex_Index_Range
- Purpose: Sets the vertex index range for rendering
- Calls: None

## Globals
- None

## Dependencies
- "meshmdl.h", "dx8list.h", "sortingrenderer.h", "mesh.h", "dx8wrapper.h"
- DX8Wrapper, SortingRendererClass, MeshModelClass, MultiListObjectClass
