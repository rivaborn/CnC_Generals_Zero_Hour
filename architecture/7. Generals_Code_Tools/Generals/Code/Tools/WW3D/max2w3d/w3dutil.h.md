# Generals/Code/Tools/WW3D/max2w3d/w3dutil.h

## Purpose
Header file defining utility structures and functions for the W3D exporter plugin in 3ds Max.

## Responsibilities
- Declares the `W3dExportOptionsStruct` for storing export settings
- Provides accessor functions for W3D AppData attached to nodes
- Defines the utility class ID for the exporter
- Includes necessary headers for MAXScript integration

## Key Types
- **W3dExportOptionsStruct (struct)**: Stores export settings for hierarchy, animation, and geometry options
- **W3DAppData0Struct (struct)**: Not inferable (defined elsewhere)
- **W3DAppData1Struct (struct)**: Not inferable (defined elsewhere)
- **W3DDazzleAppDataStruct (struct)**: Not inferable (defined elsewhere)

## Key Functions
### Get_W3D_Utility_Desc
- Purpose: Returns the ClassDesc for the W3D utility plugin
- Calls: None

### GetW3DAppData0
- Purpose: Accessor for W3DAppData0Struct attached to a node
- Calls: None

### GetW3DAppData1
- Purpose: Accessor for W3DAppData1Struct attached to a node
- Calls: None

### GetW3DDazzleAppData
- Purpose: Accessor for W3DDazzleAppDataStruct attached to a node
- Calls: None

## Globals
- **W3DUtilityClassID (Class_ID)**: Unique identifier for the W3D utility class

## Dependencies
- `<Max.h>`: 3ds Max SDK headers
- `"utilapi.h"`: Utility API definitions
- `"dllmain.h"`: DLL entry point definitions
- `"resource.h"`: Resource
