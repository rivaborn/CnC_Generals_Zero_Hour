# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/dx8renderer.cpp

## Purpose
Implements the DirectX 8 mesh renderer for the SAGE engine, handling 3D mesh rendering, material passes, and texture management.

## Responsibilities
- Manages mesh registration and rendering
- Handles material passes and texture categories
- Implements rendering tasks for polygons and materials
- Manages vertex buffers and index buffers
- Provides statistics logging for debugging

## Key Types
- **PolyRenderTaskClass (Class)**: Tracks polygon renderers and meshes needing rendering
- **MatPassTaskClass (Class)**: Tracks material passes needing rendering
- **DX8TextureCategoryClass (Class)**: Manages texture categories for rendering
- **DX8FVFCategoryContainer (Class)**: Container for meshes with similar FVF (Flexible Vertex Format)
- **Vertex_Split_Table (Class)**: Manages vertex data splitting for rendering
- **Textures_Material_And_Shader_Booking_Struct (Class)**: Books textures, materials, and shaders

## Key Functions
### Equal_Material
- Purpose: Compares two vertex materials for equality
- Calls: None

### Add_Rigid_Mesh_To_Container
- Purpose: Adds a rigid mesh to the appropriate FVF category container
- Calls: DX8FVFCategoryContainer::Check_If_Mesh_Fits, DX8FVFCategoryContainer::Add_Mesh

### Render_FVF_Category_Container_List
- Purpose: Renders all containers in an FVF category list
- Calls: DX8FVFCategoryContainer::Render

### Render_FVF_Category_Container_List_Delayed_Passes
- Purpose: Renders delayed material passes for all containers in an FVF category list
- Calls: DX8FVFCategoryContainer::Render_Delayed_Procedural_Material_Passes

### Log_Container_List
- Purpose: Logs statistics for all containers in an FVF category list
- Calls: DX8FVFCategoryContainer::Log

### Invalidate_FVF_Category_Container_List
- Purpose: Invalidates and deletes all containers in an FVF category list
- Calls: None

## Globals
- **TheDX8MeshRenderer (DX8MeshRendererClass)**: Global instance of the DX8 mesh renderer
- **_TempVertexBuffer (DynamicVectorClass<Vector3>)**: Temporary buffer for vertex data
- **_TempNormalBuffer (DynamicVectorClass<Vector3>)**: Temporary buffer for normal data
- **_RegisteredMeshList (MultiListClass<MeshModelClass>)**: List of registered mesh models
- **texture_category_delete_list (TextureCategoryList)**: List of texture categories pending deletion
- **fvf_category_container_delete_list (FVFCategoryList)**: List of FVF category containers pending deletion
- **MAX_ADDED_TYPE_COUNT (int)**: Maximum number of added types
- **statistics_requested (unsigned)**: Flag for requesting statistics logging

## Dependencies
- dx8renderer.h, dx8wrapper.h, dx8polygonrenderer.h, dx8vertexbuffer.h, dx8indexbuffer.h, dx8fvf.h, dx8caps.h, dx8rendererdebugger.h, wwdebug.h, wwprofile.h, wwmemlog.h, rinfo.h, statistics.h, meshmdl.h, vp.h, decalmsh.h, matpass.h, camera.h, stripoptimizer.h, meshgeometry.h
