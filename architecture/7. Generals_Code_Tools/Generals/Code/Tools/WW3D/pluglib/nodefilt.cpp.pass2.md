# Generals/Code/Tools/WW3D/pluglib/nodefilt.cpp - Enhanced Analysis

## Architectural Role
This file implements node filtering logic for the WW3D plugin system, enabling selective traversal of 3D scene graphs during asset processing. It bridges the Max SDK (via INode/Object) with the WW3D pipeline, providing type-safe node selection for mesh/animation export.

## Cross-References
### Incoming
- **WW3D exporter tools**: Likely call these filters during scene traversal for asset collection
- **Max plugin infrastructure**: Uses IStdPlug interface for node evaluation

### Outgoing
- **Max SDK**: Directly uses INode, Object, and controller interfaces
- **WW3D core**: Filter results feed into asset serialization pipeline

## Design Patterns
- **Strategy Pattern**: Each filter class implements `Accept_Node` with different criteria, allowing dynamic selection behavior
- **Composite Pattern**: Filters can be combined (e.g., `VisibleMeshOrHelperINodeFilter`) to create complex selection logic
- **Null Object Pattern**: Default filter instance (`DefaultINodeFilter`) provides sensible defaults

*Key insight*: The commented visibility checks (`GetVisibility`) suggest this code was adapted from earlier versions where visibility was more granularly controlled.
