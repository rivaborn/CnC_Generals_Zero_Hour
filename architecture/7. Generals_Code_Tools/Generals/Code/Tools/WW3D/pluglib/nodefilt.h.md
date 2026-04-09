# Generals/Code/Tools/WW3D/pluglib/nodefilt.h

## Purpose
Defines a node filtering interface and concrete implementations for 3DS Max plugin integration.

## Responsibilities
- Declares abstract `INodeFilterClass` interface for node filtering.
- Provides concrete filter classes for different node types (mesh, helper, animated, etc.).
- Supports visibility and selection state filtering.
- Used in Max plugin context for scene node processing.

## Key Types
- **INodeFilterClass (Class)**: Abstract base class for node filtering logic.
- **AnyINodeFilter (Class)**: Accepts all nodes.
- **HelperINodeFilter (Class)**: Filters helper objects.
- **MeshINodeFilter (Class)**: Filters triangle meshes.
- **VisibleMeshINodeFilter (Class)**: Filters visible triangle meshes.
- **VisibleHelperINodeFilter (Class)**: Filters visible helper objects.
- **VisibleMeshOrHelperINodeFilter (Class)**: Filters visible meshes or helpers.
- **AnimatedINodeFilter (Class)**: Filters nodes with animation keys.
- **VisibleSelectedINodeFilter (Class)**: Filters visible and selected nodes.

## Key Functions
### INodeFilterClass::Accept_Node
- Purpose: Abstract method to determine if a node should be accepted.
- Calls: None (pure virtual).

### AnyINodeFilter::Accept_Node
- Purpose: Always accepts nodes.
- Calls: None.

### HelperINodeFilter::Accept_Node
- Purpose: Accepts helper nodes.
- Calls: Not inferable (implementation in .cpp).

### MeshINodeFilter::Accept_Node
- Purpose: Accepts triangle mesh nodes.
- Calls: Not inferable.

### VisibleMeshINodeFilter::Accept_Node
- Purpose: Accepts visible triangle mesh nodes.
- Calls: Not inferable.

### VisibleHelperIN
