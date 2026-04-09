# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/dx8renderer.h

## Purpose
Header file defining the DirectX 8 mesh rendering system for the SAGE engine, including texture categories, FVF containers, and the main mesh renderer.

## Responsibilities
- Declares classes for DirectX 8 rendering pipeline
- Defines texture and material management structures
- Specifies mesh rendering containers for rigid and skinned meshes
- Declares the global mesh renderer instance

## Key Types
- **DX8TextureCategoryClass (Class)**: Manages texture-material-shader combinations for batch rendering
- **DX8FVFCategoryContainer (Class)**: Base class for FVF-based rendering containers
- **DX8RigidFVFCategoryContainer (Class)**: Container for non-skinned mesh rendering
- **DX8SkinFVFCategoryContainer (Class)**: Container for skinned mesh rendering
- **DX8MeshRendererClass (Class)**: Main mesh rendering controller
- **MAX_PASSES (Enum)**: Defines maximum render passes (4)

## Key Functions
### DX8TextureCategoryClass::Render
- Purpose: Renders all polygon renderers in this texture category
- Calls: Not inferable

### DX8FVFCategoryContainer::Render
- Purpose: Virtual render method for FVF containers
- Calls: Not inferable

### DX8MeshRendererClass::Render_Decal_Meshes
- Purpose: Renders decal meshes in the scene
- Calls: Not inferable

## Globals
- **TheDX8MeshRenderer (DX8MeshRendererClass)**: Global instance of the mesh renderer

## Dependencies
- "always.h", "wwstring.h", "simplevec.h", "refcount.h", "vector.h", "dx8list.h", "shader.h", "dx8wrapper.h", "meshmatdesc.h"
- IndexBufferClass, VertexBufferClass, MeshClass, CameraClass, etc. (forward declarations)
