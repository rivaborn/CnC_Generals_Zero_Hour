# Generals/Code/Tools/WW3D/max2w3d/meshcon.h - Enhanced Analysis

## Architectural Role
This file defines the core data structures for the 3DS Max to W3D model export pipeline, bridging the Max SDK's hierarchy system with the W3D runtime format. It serves as the intermediate representation for skeletal animations and mesh attachments.

## Cross-References
### Incoming
- Likely called by `max2w3d` export tools and W3D model compilers
- Used by hierarchy processing modules in the asset pipeline

### Outgoing
- Depends on `GeometryExportTaskClass` and `GeometryExportContextClass` for export workflow
- Uses `DynamicVectorClass` for container management
- Interfaces with Max SDK's `INode` system

## Design Patterns
- **Composite Pattern**: `MeshConnectionsClass` aggregates different types of mesh connections (sub-objects, aggregates, proxies) into a hierarchical structure
- **Data Transfer Object (DTO)**: `ConnectionStruct` acts as a lightweight container for mesh-bone associations during export
- **Adapter Pattern**: Bridges Max's node hierarchy with W3D's bone system through `BoneIndex` mapping

Rules followed. Output under 400 tokens.
