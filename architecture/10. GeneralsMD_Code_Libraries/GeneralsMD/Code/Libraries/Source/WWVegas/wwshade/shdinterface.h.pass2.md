# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdinterface.h - Enhanced Analysis

## Architectural Role
This file defines the core shader interface for the SAGE engine's rendering pipeline, serving as the abstraction layer between shader implementations and the rendering system. It enables the engine to support multiple shader types while maintaining a consistent interface for vertex processing, texture management, and render state application.

## Cross-References
### Incoming
- Rendering subsystem (calls shader methods for mesh rendering)
- Resource management (uses shader definitions for texture/vertex stream handling)
- Modding infrastructure (extends shader interface for custom shaders)

### Outgoing
- **ShdDefClass**: Shader definition management
- **ShdMeshClass**: Mesh rendering operations
- **RenderInfoClass**: Render state configuration
- **TextureClass**: Texture resource access
- **dx8wrapper.h**: DirectX 8 integration

## Design Patterns
- **Strategy Pattern**: Shader implementations are interchangeable strategies for rendering operations
- **Factory Pattern**: Shaders are created via associated ShdDefClass instances
- **Template Method**: Core rendering flow defined in base class with hooks for customization

*Not inferable*: Specific shader implementations or rendering pipeline details.
