# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdinterface.cpp - Enhanced Analysis

## Architectural Role
This file implements the base class for shader interfaces in the SAGE engine's rendering pipeline, serving as an abstraction layer between shader definitions and their runtime instances. It manages reference-counted pointers to shader definitions, enabling efficient sharing and memory management across the rendering system.

## Cross-References
### Incoming
- Rendering subsystem (W3D) likely instantiates ShdInterfaceClass derivatives for material/shader management
- Shader definition system (ShdDefClass) is referenced but not instantiated here

### Outgoing
- Uses reference counting macros (REF_PTR_SET/REF_PTR_RELEASE) from WWVegas memory management
- Depends on ShdDefClass for shader definition data (forward declared in header)

## Design Patterns
- **Reference Counting**: Manages shader definition lifetimes via REF_PTR macros, enabling shared ownership
- **Interface/Implementation Separation**: Base class defines common shader interface while allowing derived classes to implement specific shader types
- **Resource Management**: Encapsulates shader definition access through Peek_Definition, enforcing const-correctness for read-only access
