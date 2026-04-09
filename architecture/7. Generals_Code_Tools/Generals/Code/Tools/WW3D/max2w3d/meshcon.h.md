# Generals/Code/Tools/WW3D/max2w3d/meshcon.h

## Purpose
Defines classes for managing mesh connections and hierarchy in 3D model export for the W3D format.

## Responsibilities
- Define `ConnectionStruct` to store bone/mesh associations
- Implement `MeshConnectionsClass` to manage hierarchical model descriptions
- Provide accessors for mesh data and hierarchy information
- Support dynamic vector operations for mesh connections

## Key Types
- `ConnectionStruct` (struct): Stores bone index, object name, and INode pointer for mesh connections
- `MeshConnectionsClass` (class): Manages hierarchical model descriptions with sub-objects, aggregates, and proxies
- `GeometryExportTaskClass` (forward declared): Used for sub-object management
- `GeometryExportContextClass` (forward declared): Used for export context

## Key Functions
### `MeshConnectionsClass::Get_Sub_Object_Data`
- Purpose: Retrieves data for a sub-object at the given index
- Calls: None visible

### `MeshConnectionsClass::Get_Aggregate_Data`
- Purpose: Retrieves data for an aggregate at the given index
- Calls: None visible

### `MeshConnectionsClass::Get_Proxy_Data`
- Purpose: Retrieves data for a proxy object at the given index
- Calls: None visible

## Globals
- None

## Dependencies
- `always.h`, `chunkio.h`, `nodelist.h`, `hiersave.h`, `w3d_file.h`, `vector.h`
- `DynamicVectorClass`, `INode`, `W3D_NAME_LEN`
