# Generals/Code/Tools/WW3D/max2w3d/meshcon.cpp - Enhanced Analysis

## Architectural Role
This file is part of the 3DS Max to W3D exporter toolchain, specifically handling the hierarchical relationships between mesh components (sub-objects, aggregates, and proxy objects). It bridges the Max scene graph with the W3D format's skeletal structure by managing bone attachments and object references.

## Cross-References
### Incoming
- Likely called by the main exporter logic (e.g., `geometryexporttask.cpp`) to query mesh connection data during W3D export
- May be referenced by validation tools checking mesh hierarchy integrity

### Outgoing
- Calls into `GeometryExportTaskClass` methods (`Get_Full_Name`, `Get_Bone_Index`, etc.) to populate connection data
- Uses `GeometryExportContextClass` for time/origin context
- Relies on `DynamicVectorClass` for dynamic array management

## Design Patterns
- **Composite Pattern**: Manages hierarchical mesh relationships (sub-objects, aggregates, proxies) as separate collections
- **Data Access Object (DAO)**: Provides controlled access to connection data via getter methods
- **Factory Method**: Constructor acts as a factory, initializing connections from export tasks (not inferable if tasks are pre-created)

*Not inferable*: No clear use of Observer, Strategy, or Visitor patterns.
