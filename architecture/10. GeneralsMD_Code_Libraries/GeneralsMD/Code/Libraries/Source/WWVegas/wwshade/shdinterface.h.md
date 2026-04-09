# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdinterface.h

## Purpose
Defines the shader interface for the SAGE engine, including core classes and structures for shader management.

## Responsibilities
- Declares shader interface classes and structures
- Defines vertex stream data structure
- Specifies shader comparison and rendering methods
- Establishes shader texture and vertex stream handling

## Key Types
- **ShdDefClass (Class)**: Shader definition base class
- **ShdMeshClass (Class)**: Mesh class for shader application
- **RenderInfoClass (Class)**: Rendering information container
- **TextureClass (Class)**: Texture resource class
- **VertexStreamStruct (Struct)**: Container for vertex stream data (positions, normals, UVs, colors)
- **ShdInterfaceClass (Class)**: Virtual interface for all shaders with rendering setup methods

## Key Functions
### ShdInterfaceClass::Peek_Definition
- Purpose: Access shader definition
- Calls: None

### ShdInterfaceClass::Get_Class_ID
- Purpose: Get shader class identifier
- Calls: None

### ShdInterfaceClass::Greater_Than
- Purpose: Compare shaders for sorting
- Calls: None

### ShdInterfaceClass::Similar_Enough
- Purpose: Check if shaders are similar enough for batching
- Calls: None

### ShdInterfaceClass::Get_Pass_Count
- Purpose: Get number of render passes
- Calls: None

### ShdInterfaceClass::Pass_Selection
- Purpose: Select appropriate render pass
- Calls: None

### ShdInterfaceClass::Apply_Shared
- Purpose: Apply shared render states
- Calls: None

### ShdInterfaceClass::Apply_Instance
- Purpose: Apply instance-specific render states
- Calls: None

### Shd
