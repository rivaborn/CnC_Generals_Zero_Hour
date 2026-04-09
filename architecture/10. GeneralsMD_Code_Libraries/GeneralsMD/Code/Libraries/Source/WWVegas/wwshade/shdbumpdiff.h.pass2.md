# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdbumpdiff.h - Enhanced Analysis

## Architectural Role
This file defines the bump-mapped diffuse shader class within the SAGE engine's rendering pipeline, extending the base shader definition system. It bridges the gap between shader configuration and hardware-specific implementation, supporting the engine's modular rendering architecture.

## Cross-References
### Incoming
- **Shader Factory**: Likely called by the shader creation system when instantiating bump-mapped diffuse shaders
- **Editor Tools**: Used by level editors or shader editors for configuration
- **Save/Load System**: Invoked during game save/load operations for serialization

### Outgoing
- **Base Shader Class**: Inherits from `ShdDefClass` and uses its interface
- **Save/Load System**: Calls `ChunkSaveClass`/`ChunkLoadClass` for persistence
- **Rendering Pipeline**: Interfaces with hardware-specific shader creation

## Design Patterns
- **Factory Pattern**: `Create()` method generates shader instances, decoupling creation from implementation
- **Composite Pattern**: Extends base shader class, contributing to the engine's hierarchical shader system
- **Property Pattern**: Encapsulates shader parameters (textures, lighting) with getter/setter methods for configuration

*Not inferable*: Specific hardware abstraction details or shader program generation.
