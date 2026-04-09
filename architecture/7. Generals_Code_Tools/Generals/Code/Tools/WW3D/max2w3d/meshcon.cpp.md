# Generals/Code/Tools/WW3D/max2w3d/meshcon.cpp

## Purpose
Handles mesh connections and relationships in the 3DS Max to W3D exporter tool.

## Responsibilities
- Manages sub-objects, aggregates, and proxy objects in a mesh hierarchy
- Provides access to connection data (names, bone indices, nodes)
- Initializes connection data from geometry export tasks

## Key Types
- **MeshConnectionsClass (Class)**: Main class managing mesh connections
- **ConnectionStruct (Struct)**: Stores object name, bone index, and node reference
- **DynamicVectorClass (Template)**: Used for storing connection lists

## Key Functions
### MeshConnectionsClass::MeshConnectionsClass
- Purpose: Constructor that initializes connection data from export tasks
- Calls: `Set_W3D_Name`, `Get_Full_Name`, `Get_Bone_Index`, `Get_Object_Node`, `Is_Aggregate`, `Is_Proxy`

### MeshConnectionsClass::Get_Sub_Object_Data
- Purpose: Retrieves connection data for a sub-object by index
- Calls: None

### MeshConnectionsClass::Get_Aggregate_Data
- Purpose: Retrieves connection data for an aggregate by index
- Calls: None

### MeshConnectionsClass::Get_Proxy_Data
- Purpose: Retrieves connection data for a proxy object by index
- Calls: None

## Globals
- **CurTime (TimeValue)**: Current time value from export context
- **Origin (INode**)**: Reference to the origin node
- **Name (char[256])**: Model name buffer

## Dependencies
- `meshcon.h`, `util.h`, `SnapPoints.h`, `w3dappdata.h`, `geometryexporttask.h`, `geometryexportcontext.h`
- `DynamicVectorClass`, `GeometryExportTaskClass`, `Geometry
