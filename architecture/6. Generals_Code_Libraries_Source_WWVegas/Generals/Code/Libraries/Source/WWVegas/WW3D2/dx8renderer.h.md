# Generals/Code/Libraries/Source/WWVegas/WW3D2/dx8renderer.h

## Purpose
Header file defining DirectX 8 rendering system classes for mesh rendering in the SAGE engine.

## Responsibilities
- Declares mesh rendering classes (buffers, categories, renderers)
- Defines texture/material management for batching
- Provides global mesh renderer interface (TheDX8MeshRenderer)
- Handles rigid and skinned mesh rendering containers

## Key Types
- **DX8TextureCategoryClass (Class)**: Manages texture/shader/material batches for rendering
- **DX8FVFCategoryContainer (Class)**: Base class for FVF-based rendering containers
- **DX8RigidFVFCategoryContainer (Class)**: Container for non-skinned meshes
- **DX8SkinFVFCategoryContainer (Class)**: Container for skinned meshes
- **DX8MeshRendererClass (Class)**: Global mesh rendering controller
- **MAX_PASSES (Enum)**: Defines maximum render passes (4)

## Key Functions
### DX8TextureCategoryClass::Render
- Purpose: Renders all polygon renderers in this texture category
- Calls: Not inferable (implementation in .cpp)

### DX8FVFCategoryContainer::Add_Mesh
- Purpose: Adds a mesh model to the appropriate texture category
- Calls: Generate_Texture_Categories, Insert_To_Texture_Category

### DX8MeshRendererClass::Register_Mesh_Type
- Purpose: Registers a mesh model type with the renderer
- Calls: Not inferable

## Globals
- **TheDX8MeshRenderer (DX8MeshRendererClass)**: Global instance of the mesh renderer

## Dependencies
- Key includes: "always.h", "wwstring.h", "simplevec.h", "refcount.h", "vector.h", "dx8list.h", "shader.h", "dx8wrapper.h"
- External symbols: MultiListObjectClass, MeshModelClass, CameraClass, etc.
