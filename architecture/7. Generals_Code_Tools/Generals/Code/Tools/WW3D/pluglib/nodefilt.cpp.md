# Generals/Code/Tools/WW3D/pluglib/nodefilt.cpp

## Purpose
Implements various node filters for 3D scene graph traversal in the WW3D plugin system.

## Responsibilities
- Defines node filter classes for selecting different types of scene nodes
- Implements acceptance criteria for visible meshes, helpers, and animated nodes
- Provides default filter instance
- Handles node visibility and selection checks

## Key Types
- **HelperINodeFilter (Class)**: Filters helper objects (including hidden ones)
- **MeshINodeFilter (Class)**: Filters mesh objects (including hidden ones)
- **VisibleMeshINodeFilter (Class)**: Filters visible mesh objects
- **VisibleHelperINodeFilter (Class)**: Filters visible helper objects
- **VisibleMeshOrHelperINodeFilter (Class)**: Filters visible mesh or helper objects
- **AnimatedINodeFilter (Class)**: Filters animated nodes with animation keys
- **VisibleSelectedINodeFilter (Class)**: Filters visible and selected nodes

## Key Functions
### HelperINodeFilter::Accept_Node
- Purpose: Checks if node is a helper object
- Calls: node->EvalWorldState, obj->SuperClassID

### MeshINodeFilter::Accept_Node
- Purpose: Checks if node is a mesh object convertible to tri-mesh
- Calls: node->EvalWorldState, obj->CanConvertToType, obj->SuperClassID

### VisibleMeshINodeFilter::Accept_Node
- Purpose: Checks if node is a visible mesh object
- Calls: node->EvalWorldState, node->IsHidden, obj->CanConvertToType, obj->SuperClassID

### VisibleHelperINodeFilter::Accept_Node
- Purpose: Checks if node is a visible helper object
- Calls: node->EvalWorldState, node->IsHidden, obj->SuperClassID

### VisibleMeshOrHelperINodeFilter::Accept_Node
- Purpose: Checks if node is a visible mesh or helper object
- Calls: node->EvalWorldState, node->IsHidden, obj->CanConvertToType, obj->SuperClassID

### AnimatedINodeFilter::Accept_Node
- Purpose: Checks if node is animated with animation keys
- Calls: node->EvalWorldState, node->IsHidden, node->GetTMController, GetKeyControlInterface

### VisibleSelectedINodeFilter::Accept_Node
- Purpose: Checks if node is visible and selected
- Calls: node->IsHidden, node->Selected

## Globals
- **DefaultINodeFilter (VisibleMeshINodeFilter)**: Default node filter instance

## Dependencies
- nodefilt.h
- istdplug.h
- INode, Object, TimeValue, triObjectClassID, GEOM
