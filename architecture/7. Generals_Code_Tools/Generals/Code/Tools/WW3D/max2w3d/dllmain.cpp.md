# Generals/Code/Tools/WW3D/max2w3d/dllmain.cpp

## Purpose
This file implements the DLL entry point and plugin interface for the 3DS Max exporter plugin for W3D (Westwood 3D) models.

## Responsibilities
- Provides DLL initialization and cleanup
- Exposes plugin metadata (description, version, class count)
- Registers W3D export-related classes with 3DS Max
- Manages plugin resource strings

## Key Types
- W3dClassDesc (struct): Descriptor for the W3D export class
- None: No other classes/structs/enums defined in this file

## Key Functions
### DllMain
- Purpose: DLL entry point that initializes plugin controls
- Calls: InitCustomControls, InitCommonControls

### LibDescription
- Purpose: Returns the plugin description string
- Calls: Get_String

### LibNumberClasses
- Purpose: Returns the number of classes exported by this plugin
- Calls: None

### LibClassDesc
- Purpose: Returns ClassDesc for the specified plugin class
- Calls: Get_W3D_Utility_Desc, Get_Skin_Obj_Desc, Get_Skin_Mod_Desc, Get_Game_Material_Desc, Get_Game_Maps_Desc, Get_PS2_Game_Material_Desc, Get_PS2_Material_Conversion, Get_Alpha_Desc

### LibVersion
- Purpose: Returns the plugin version number
- Calls: None

### Get_String
- Purpose: Loads a string from plugin resources
- Calls: LoadString

## Globals
- AppInstance (HINSTANCE): Stores the DLL instance handle
- ControlsInit (int): Tracks whether controls have been initialized
- W3d_Export_Class_Descriptor (W3dClassDesc): Descriptor for the main W3D export class

## Dependencies
- Max.h: 3DS Max SDK headers
- dllmain.h: Local header for this module
- w3ddesc.h, w3dexp.h, w3dutil.h: W3D export-related headers
- skin.h, gamemtl.h, gamemaps.h: Material and skinning headers
- MeshDeform.H, AlphaModifier.h, gridsnapmodifier.h: Modifier headers
- resource.h: Resource IDs
- <stdio.h>: Standard I/O (for printf/LoadString)
