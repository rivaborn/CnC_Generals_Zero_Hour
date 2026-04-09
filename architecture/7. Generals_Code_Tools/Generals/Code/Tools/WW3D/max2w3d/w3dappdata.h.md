# Generals/Code/Tools/WW3D/max2w3d/w3dappdata.h

## Purpose
Defines data structures and utility functions for 3DS Max plugin used to export W3D (Westwood 3D) model data.

## Responsibilities
- Declares app-data structures for W3D export options
- Provides utility functions to check node export properties
- Defines enums for geometry types, export flags, and collision flags
- Manages versioning and compatibility for app-data structures

## Key Types
- **W3DAppData0Struct (Class)**: Obsolete app-data structure for basic export flags
- **W3DAppData1Struct (Class)**: Stores damage region information for objects
- **W3DAppData2Struct (Class)**: Main app-data structure containing all export options
- **GeometryTypeEnum (Enum)**: Defines types of geometry (mesh, collision, etc.)
- **ExportFlagsEnum (Enum)**: Bit flags for export options
- **GeometryFlagsEnum (Enum)**: Bit flags for geometry-specific options
- **CollisionFlagsEnum (Enum)**: Bit flags for collision properties
- **W3DDazzleAppDataStruct (Class)**: Stores dazzle-specific render parameters

## Key Functions
### Is_Bone
- Purpose: Checks if a node should be exported as a bone/transform
- Calls: Not inferable

### Is_Geometry
- Purpose: Checks if a node should have its geometry exported
- Calls: Not inferable

### Is_Proxy
- Purpose: Checks if a node is a proxy (contains '~' in name)
- Calls: strchr

### W3DAppData2Struct::Get_App_Data
- Purpose: Retrieves or creates app-data for a given node
- Calls: Not inferable

### W3DDazzleAppDataStruct::Get_App_Data
- Purpose: Retrieves or creates dazzle app-data for a given node
- Calls: Not inferable

## Globals
- **W3D_APPDATA_0 (const)**: App-data chunk ID for obsolete structure
- **W3D_APPDATA_1 (const)**: App-data chunk ID for damage region data
- **W3D_APPDATA_2 (const)**: App-data chunk ID for main export options
- **W3D_DAZZLE_APPDATA (const)**: App-data chunk ID for dazzle parameters
- **MAX_DAMAGE_REGIONS (const)**: Maximum number of damage regions
- **NO_DAMAGE_REGION (const)**: Value indicating no damage region

## Dependencies
- `<Max.h>`: 3DS Max SDK header
- `strchr`: C string function for proxy detection
