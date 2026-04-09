# Generals/Code/Tools/WW3D/max2w3d/w3dutil.cpp

## Purpose
Provides utility functionality for W3D export in 3DS Max, including UI controls and node state management.

## Responsibilities
- Manages W3D export settings UI
- Handles node selection and state evaluation
- Provides material conversion utilities
- Implements name generation for nodes and materials
- Manages dazzle effects and collision settings

## Key Types
- **MaterialReferenceMaker (Class)**: Manages material references for export utilities
- **SettingsFormClass (Class)**: Handles the settings dialog UI
- **W3DUtilityClass (Class)**: Main utility plugin class for W3D export options
- **NodeStatesStruct (Struct)**: Contains export state information for nodes
- **MaterialConversionEnum (Enum)**: Defines material conversion types

## Key Functions
### eval_tri_state
- Purpose: Evaluates tri-state checkbox values
- Calls: None

### eval_node_states
- Purpose: Evaluates the export states of nodes in a list
- Calls: None

### update_settings_controls
- Purpose: Updates controls in active settings panels
- Calls: None

### set_hierarchy_in_all_selected
- Purpose: Modifies hierarchy state for all selected nodes
- Calls: None

### generate_names
- Purpose: Generates names for selected nodes
- Calls: generate_node_name

### export_with_standard_materials
- Purpose: Exports with standard materials
- Calls: convert_materials

### get_app_data_0/1/2
- Purpose: Retrieves W3D app data from nodes
- Calls: None

## Globals
- **_INodeFilter (VisibleSelectedINodeFilter)**: Node filter for selection
- **TheW3DUtility (W3DUtilityClass)**: Singleton instance of the utility
- **W3DUtilityDesc (W3DUtilityClassDesc)**: Class descriptor for the utility

## Dependencies
- w3dutil.h, w3ddesc.h, rcmenu.h, util.h, nodelist.h, tchar.h, gamemtl.h, notify.h, gennamesdialog.h, genmtlnamesdialog.h, genlodextensiondialog.h, floaterdialog.h, <StdMat.h>
