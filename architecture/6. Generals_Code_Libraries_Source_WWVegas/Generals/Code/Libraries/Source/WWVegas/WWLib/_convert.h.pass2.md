# Generals/Code/Libraries/Source/WWVegas/WWLib/_convert.h - Enhanced Analysis

## Architectural Role
This header serves as a central registry for global rendering converter instances, bridging the W3D rendering subsystem with the game's rendering pipeline. It provides external access to specialized converters for different rendering modes (voxels, units, terrain, etc.), which are likely used during scene composition and rendering passes.

## Cross-References
### Incoming
- W3D rendering subsystem (e.g., `W3D.cpp`, `Scene.cpp`) likely references these globals during render setup
- Game logic components (e.g., `Unit.cpp`, `Building.cpp`) may access these for specialized rendering

### Outgoing
- Includes `convert.h`, implying dependency on the base `ConvertClass` definition
- No direct outgoing references to other subsystems (header-only)

## Design Patterns
- **Registry Pattern**: Global instances act as a registry for different converter types
- **Dependency Injection**: Converters are injected into rendering pipeline via these globals
- **Not inferable**: No clear factory pattern (instances appear pre-initialized elsewhere)

*Token count: 198*
