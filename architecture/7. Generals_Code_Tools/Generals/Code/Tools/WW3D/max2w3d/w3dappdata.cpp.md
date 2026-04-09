# Generals/Code/Tools/WW3D/max2w3d/w3dappdata.cpp

## Purpose
Handles W3D export data structures and utility functions for 3DS Max scene nodes.

## Responsibilities
- Manages W3DAppData2Struct and W3DDazzleAppDataStruct classes
- Provides utility functions to check node properties (bones, geometry, collision, etc.)
- Handles version migration for app data structures
- Retrieves and creates app data chunks for Max nodes

## Key Types
- W3DAppData2Struct (Class): Stores export flags and geometry/collision settings for nodes
- W3DDazzleAppDataStruct (Class): Stores dazzle-specific export data
- W3DAppData0Struct (Class): Legacy app data structure (referenced but not defined here)

## Key Functions
### get_geometry_type
- Purpose: Retrieves geometry type from node's app data
- Calls: W3DAppData2Struct::Get_App_Data, Get_Geometry_Type

### Is_Bone
- Purpose: Checks if node is a bone (excluding skins and origins)
- Calls: Is_Skin, Is_Origin, W3DAppData2Struct::Get_App_Data, Is_Bone

### Is_Geometry
- Purpose: Checks if node is marked for geometry export
- Calls: W3DAppData2Struct::Get_App_Data, Is_Geometry

### Is_Normal_Mesh
- Purpose: Checks if node is a normal mesh (excluding skins and proxies)
- Calls: Is_Geometry, Is_Skin, Is_Proxy, get_geometry_type

### Is_Camera_Aligned_Mesh
- Purpose: Checks if node is a camera-aligned mesh
- Calls: Is_Geometry, get_geometry_type

### Is_Camera_Oriented_Mesh
- Purpose: Checks if node is a camera-oriented mesh
- Calls: Is_Geometry, get_geometry_type

### Is_Collision_AABox
- Purpose: Checks if node is an axis-aligned collision box
- Calls: Is_Geometry, get_geometry_type

### Is_Collision_OBBox
- Purpose: Checks if node is an oriented bounding box collision
- Calls: Is_Geometry, get_geometry_type

### Is_Skin
- Purpose: Checks if node contains skin modifier
- Calls: Is_Geometry, get_geometry_type, node->NumRefs, node->GetReference, WSM_DERIVOB_CLASS_ID, SKIN_MOD_CLASS_ID

### Is_Shadow
- Purpose: Checks if node is marked to cast shadows
- Calls: Is_Geometry, W3DAppData2Struct::Get_App_Data, Is_Shadow_Enabled

### Is_Null_Object
- Purpose: Checks if node is a null object
- Calls: Is_Geometry, get_geometry_type

### Is_Dazzle
- Purpose: Checks if node is a dazzle object
- Calls: Is_Geometry, get_geometry_type

### Is_Aggregate
- Purpose: Checks if node is an aggregate object
- Calls: Is_Geometry, get_geometry_type

### Is_Physical_Collision
- Purpose: Checks if node has physical collision enabled
- Calls: W3DAppData2Struct::Get_App_Data, Is_Physical_Collision_Enabled

### Is_Projectile_Collision
- Purpose: Checks if node has projectile collision enabled
- Calls: W3DAppData2Struct::Get_App_Data, Is_Projectile_Collision_Enabled

### Is_Vis_Collision
- Purpose: Checks if node has visibility collision enabled
- Calls
