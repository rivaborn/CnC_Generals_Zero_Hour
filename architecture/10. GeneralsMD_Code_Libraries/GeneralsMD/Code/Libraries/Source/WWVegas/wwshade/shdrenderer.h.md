# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdrenderer.h

## Purpose
Defines the shader rendering system for the SAGE engine, including renderer nodes, containers, and the main renderer interface.

## Responsibilities
- Manages shader-based rendering pipeline
- Handles mesh registration and rendering
- Provides multi-pass rendering support
- Implements reference counting for resources
- Supports DirectX 8 renderer implementation

## Key Types
- **ShdRendererNodeClass (Class)**: Abstract base for rendering nodes that link meshes to the rendering system
- **RendererListContainerClass (Class)**: Manages linked and visible renderer nodes per pass
- **ShdRendererClass (Class)**: Abstract base for the main renderer interface
- **ShdDX8RendererClass (Class)**: DirectX 8 implementation of the renderer
- **MeshContainerClass (Class)**: Internal container for mesh categories (forward declaration)

## Key Functions
### ShdRendererNodeClass::Connect
- Purpose: Adds the node to visible node lists for all passes
- Calls: RendererListContainerClass::Add_Visible_Node

### ShdRendererNodeClass::Set_Renderer_List_Container
- Purpose: Associates a renderer list container with this node for a specific pass
- Calls: REF_PTR_SET

### ShdRendererClass::Init/Shutdown
- Purpose: Initializes/shuts down the renderer system
- Calls: None visible

### ShdDX8RendererClass::Register_Mesh
- Purpose: Registers a mesh/submesh for rendering with the DX8 renderer
- Calls: Not inferable

### ShdDX8RendererClass::Flush
- Purpose: Submits all registered meshes to the rendering pipeline
- Calls: Not inferable

## Globals
- **ShdRenderer (ShdRendererClass*)**: Static instance pointer for the renderer
