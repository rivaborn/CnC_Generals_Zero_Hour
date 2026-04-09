# Generals/Code/Tools/WW3D/max2w3d/skindata.h - Enhanced Analysis

## Architectural Role
This file defines the core data structures for vertex skinning in the Max2W3D conversion pipeline, bridging 3DS Max's modifier system with the W3D format's skeletal animation requirements. It serves as the intermediary representation for bone influence data during model export.

## Cross-References
### Incoming
- **max2w3d/max2w3d.cpp**: Likely uses SkinDataClass for processing mesh data during export
- **WW3D modifier plugins**: Would reference this for runtime skinning data access
- **Serialization handlers**: Call Save/Load methods during .max file I/O

### Outgoing
- **Max SDK (Max.h)**: Uses 3DS Max's Mesh and selection APIs
- **namedsel.h**: Relies on named selection set infrastructure
- **LocalModData**: Inherits from 3DS Max's modifier data base class

## Design Patterns
- **Data Transfer Object**: SkinDataClass encapsulates skinning data for transfer between tools
- **Composite**: VertData aggregates multiple InfluenceStruct instances
- **Memento**: Save/Load methods preserve skinning state for undo/redo operations

*Not inferable: No clear use of Observer or Factory patterns in this header alone.*
