# Generals/Code/Tools/WW3D/max2w3d/geometryexportcontext.h - Enhanced Analysis

## Architectural Role
This file defines the core export context for the Max2W3D toolchain, bridging 3ds Max's SDK with the W3D asset pipeline. It serves as a container for export state, coordinating between Max's scene graph and the W3D chunk-based serialization system.

## Cross-References
### Incoming
- `Generals/Code/Tools/WW3D/max2w3d/geometryexport.cpp` (primary consumer)
- `Generals/Code/Tools/WW3D/max2w3d/materialexport.cpp` (for material color tracking)
- `Generals/Code/Tools/WW3D/max2w3d/hierarchyexport.cpp` (for hierarchy processing)

### Outgoing
- **3ds Max SDK**: `INode::GetNodeTM()`, `Matrix3` operations
- **W3D Pipeline**: `ChunkSaveClass`, `HierarchySaveClass` (chunk serialization)
- **Progress System**: `Progress_Meter_Class` (UI feedback)

## Design Patterns
- **Context Object Pattern**: Encapsulates all export-related state to avoid parameter explosion in export functions.
- **Resource Management**: Uses RAII for `ModelName` allocation/deallocation.
- **Dependency Injection**: References to external systems (Max SDK, W3D pipeline) are injected via constructor.

*Not inferable*: No clear use of Observer, Factory, or Visitor patterns.
