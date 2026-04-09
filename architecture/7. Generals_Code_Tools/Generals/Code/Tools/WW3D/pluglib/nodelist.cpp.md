# Generals/Code/Tools/WW3D/pluglib/nodelist.cpp

## Purpose
Manages a linked list of 3dsMAX scene nodes (INodes) with filtering and enumeration capabilities.

## Responsibilities
- Maintains a list of INode pointers in a linked list structure
- Supports filtering nodes via INodeFilterClass
- Provides array-like access to nodes
- Enumerates scene nodes via callback
- Supports insertion, removal, and tree traversal operations

## Key Types
- **INodeListEntryClass (Class)**: Linked list node containing an INode pointer and next pointer
- **INodeFilterClass (External)**: Abstract filter for accepting/rejecting nodes (not defined here)
- **INodeCompareClass (External)**: Comparison functor for sorting nodes (not defined here)

## Key Functions
### INodeListClass::Insert(INode * node)
- Purpose: Adds a node to the list if it passes the filter
- Calls: INodeFilter->Accept_Node()

### INodeListClass::callback(INode * node)
- Purpose: 3dsMAX enumeration callback that inserts accepted nodes
- Calls: Insert()

### INodeListClass::Add_Tree(INode * root)
- Purpose: Recursively adds all children of a node to the list
- Calls: Insert(), GetChildNode(), NumberOfChildren()

### INodeListClass::Sort(const INodeCompareClass & node_compare)
- Purpose: Sorts the node list using a comparison functor
- Calls: get_nth_item()

## Globals
- **_AnyFilter (AnyINodeFilter)**: Default filter that accepts all nodes

## Dependencies
- Key includes: "nodelist.h"
- External symbols: INode, IScene, TimeValue, TREE_CONTINUE (3dsMAX SDK types)
- External classes: INodeFilterClass, INodeCompareClass (abstract interfaces)
