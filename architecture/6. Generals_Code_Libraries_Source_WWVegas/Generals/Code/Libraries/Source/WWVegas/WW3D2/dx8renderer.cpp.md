# Generals/Code/Libraries/Source/WWVegas/WW3D2/dx8renderer.cpp

## Purpose
Implements the DirectX 8 mesh renderer for the SAGE engine, handling mesh registration, rendering, and resource management.

## Responsibilities
- Manages mesh rendering tasks and material passes
- Handles texture categories and FVF (Flexible Vertex Format) containers
- Processes rigid and skinned meshes
- Maintains render lists and decal meshes
- Provides logging and statistics for debugging

## Key Types
- **PolyRenderTaskClass (Class)**: Represents a polygon renderer task for a mesh
- **MatPassTaskClass (Class)**: Represents a material pass task for a mesh
- **Vertex_Split_Table (Class)**: Manages vertex data for mesh rendering
- **Textures_Material_And_Shader_Booking_Struct (Class)**: Tracks texture, material, and shader usage
- **DX8TextureCategoryClass (Class)**: Groups textures, materials, and shaders for rendering
- **DX8FVFCategoryContainer (Class)**: Container for meshes with the same FVF

## Key Functions
### Whatever
- Purpose: Processes polygon indices and vertices
- Calls: Not inferable

### Equal_Material
- Purpose: Compares two vertex materials by CRC
- Calls: VertexMaterialClass::Get_CRC()

### Add_Rigid_Mesh_To_Container
- Purpose: Adds a rigid mesh to the appropriate FVF container
- Calls: DX8FVFCategoryContainer::Check_If_Mesh_Fits(), DX8FVFCategoryContainer::Add_Mesh()

### Render_FVF_Category_Container_List
- Purpose: Renders all containers in an FVF category list
- Calls: DX8FVFCategoryContainer::Render()

### Log_Container_List
- Purpose: Logs information about containers in an FVF category list
- Calls: DX8FVFCategoryContainer::Log()

### Invalidate_FVF_Category_Container_List
- Purpose: Clears and deletes all containers in an FVF category list
- Calls: DX8FVFCategoryContainer destructor

## Globals
- **TheDX8MeshRenderer (DX8MeshRendererClass)**: Global instance of the mesh renderer
- **_TempVertexBuffer (DynamicVectorClass<Vector3>)**: Temporary buffer for vertex data
- **_TempNormalBuffer (DynamicVectorClass<Vector3>)**: Temporary buffer for normal data
- **_RegisteredMeshList (MultiListClass<MeshModelClass>)**: List of registered mesh models
- **texture_category_delete_list (TextureCategoryList)**: List of texture categories to delete
- **fvf_category_container_delete_list (FVFCategoryList)**: List of FVF containers to delete
- **MAX_ADDED_TYPE_COUNT (int)**: Maximum number of added types
- **statistics_requested (unsigned)**: Flag for requesting statistics

## Dependencies
- dx8renderer.h, dx8wrapper.h, dx8polygonrenderer.h, dx8vertexbuffer.h, dx8indexbuffer.h, dx8fvf.h, dx8caps.h, wwdebug.h, wwprofile.h, wwmemlog.h, rinfo.h, statistics.h, meshmdl.h, vp.h, decalmsh.h, matpass.h, camera.h, stripoptimizer.h, meshgeometry.h
