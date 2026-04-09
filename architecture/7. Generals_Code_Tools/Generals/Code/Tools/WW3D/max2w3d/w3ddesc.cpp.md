# Generals/Code/Tools/WW3D/max2w3d/w3ddesc.cpp

## Purpose
Implements the W3dClassDesc class, which serves as the plugin descriptor for the W3D exporter in 3ds Max.

## Responsibilities
- Defines plugin metadata (name, ID, category)
- Provides factory method for plugin instance creation
- Exposes plugin visibility and classification

## Key Types
- W3dClassDesc (Class): Plugin descriptor for W3D export functionality
- W3dExportClass (Class): The actual exporter class (created via factory)

## Key Functions
### Create
- Purpose: Factory method that creates a new W3dExportClass instance
- Calls: `new W3dExportClass`

### IsPublic
- Purpose: Indicates whether the plugin should be visible to users
- Calls: None

### ClassName
- Purpose: Returns the display name of the plugin
- Calls: `Get_String(IDS_W3D_SHORT_DESCRIPTION)`

### SuperClassID
- Purpose: Returns the base class ID for the plugin
- Calls: None

### ClassID
- Purpose: Returns the unique identifier for this plugin
- Calls: None

### Category
- Purpose: Returns the category string for plugin grouping
- Calls: `Get_String(IDS_SCENE_EXPORT)`

## Globals
None

## Dependencies
- `w3ddesc.h`, `w3dexp.h`, `dllmain.h`
- `SCENE_EXPORT_CLASS_ID`, `W3D_EXPORTER_CLASS_ID` (external constants)
- `Get_String()` (external string lookup function)
