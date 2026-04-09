# Generals/Code/Tools/WW3D/max2w3d/geometryexporttask.h - Enhanced Analysis

## Architectural Role
This file defines the core abstraction for geometry export tasks in the Max2W3D toolchain, bridging 3DS Max's scene graph with the W3D format's requirements. It serves as the contract between the asset pipeline and the runtime engine's expectations for model data.

## Cross-References
### Incoming
- `Generals/Code/Tools/WW3D/max2w3d/geometryexporttask.cpp` (implementation)
- `Generals/Code/Tools/WW3D/max2w3d/max2w3d.cpp` (driver for export process)
- Derived task classes (e.g., mesh, collision, aggregate handlers)

### Outgoing
- **3DS Max SDK**: `INode`, `Matrix3`, `Point3` (scene graph access)
- **W3D Format**: `w3d_file.h` (output format definitions)
- **Custom Containers**: `DynamicVectorClass` (task batching)

## Design Patterns
- **Factory Method**: `Create_Task` delegates instantiation to derived classes
- **Template Method**: `Export_Geometry` enforces export sequence while allowing specialization
- **Type Object**: RTTI enum enables runtime dispatch for geometry-specific handling

*Not inferable*: Concrete implementations of derived tasks (e.g., mesh vs. collision handlers).
