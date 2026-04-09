# Generals/Code/Tools/WW3D/max2w3d/AppData.cpp

## Purpose
Implements MAXScript extensions for Westwood's W3D exporter, handling app data operations between 3DS Max nodes.

## Responsibilities
- Copies W3D app data between nodes
- Sets origin-specific app data flags
- Retrieves hierarchy file paths from export options

## Key Types
- `W3DAppData0Struct` (Struct): Obsolete app data container
- `W3DAppData1Struct` (Struct): Primary app data container
- `W3DAppData2Struct` (Struct): Secondary app data container
- `W3DDazzleAppDataStruct` (Struct): Dazzle effect app data
- `W3dExportOptionsStruct` (Struct): Export configuration

## Key Functions
### copy_app_data_cf
- Purpose: Copies all W3D app data from source node to target node
- Calls: `GetW3DAppData0`, `GetW3DAppData1`, `GetW3DAppData2`, `GetW3DDazzleAppData`, `AddAppDataChunk`

### set_origin_app_data_cf
- Purpose: Configures app data for origin nodes (disables geometry/transform export)
- Calls: `GetW3DAppData2`, `Enable_Export_Geometry`, `Enable_Export_Transform`

### get_hierarchy_file_cf
- Purpose: Retrieves hierarchy file path from export options
- Calls: `GetScenePointer`, `GetAppDataChunk`

## Globals
- `def_visible_primitive` (Macro): Registers MAXScript functions (3 instances)

## Dependencies
- `<MaxScrpt.h>`: MAXScript API
- `<MaxObj.h>`: MAX node objects
- `<Strings.h>`: MAX string handling
- `<definsfn.h>`: MAXScript function registration
- `w3dutil.h`: W3D app data accessors
- `w3ddesc.h`: W3D data structures
