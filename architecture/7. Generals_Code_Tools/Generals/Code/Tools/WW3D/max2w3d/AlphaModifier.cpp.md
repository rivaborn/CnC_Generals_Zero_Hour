# Generals/Code/Tools/WW3D/max2w3d/AlphaModifier.cpp

## Purpose
Implements a 3DS Max modifier plugin for manipulating vertex alpha values in mesh objects.

## Responsibilities
- Modifies vertex alpha channel data in 3D meshes
- Handles UI interactions for alpha value editing
- Manages vertex selection based on alpha values
- Provides parameter block for modifier settings
- Integrates with 3DS Max's modifier system

## Key Types
- Alpha_Messages (Enum): Modifier message types (NOTHING, UPDATE_DATA, INITIALIZE, BOX_CHECKED)
- Dialog_Controls (Enum): UI control identifiers (EDIT_VALUE, FIND_CHECK_BOX)
- AlphaClassDesc (Class): Class descriptor for 3DS Max plugin registration
- AlphaModifierClass (Class): Main modifier class handling mesh modifications

## Key Functions
### ModifyObject
- Purpose: Applies alpha modifications to mesh vertices
- Calls: pblock->GetValue, mesh->vertexFloat, mesh->setVDataSupport, mesh->VertSel().Set/Clear, object->UpdateValidity

### NotifyInputChanged
- Purpose: Handles changes to input object topology/geometry/selection
- Calls: NotifyDependents

### DlgProc
- Purpose: Handles dialog box messages and UI events
- Calls: None directly visible

## Globals
- AlphaCD (AlphaClassDesc): Class descriptor instance
- alpha_param_blk (ParamBlockDesc2): Parameter block definition for modifier

## Dependencies
- AlphaModifier.h (header)
- 3DS Max SDK classes (ClassDesc2, ParamBlockDesc2, IParamMap2, etc.)
- Mesh/vertex manipulation APIs (TriObject, Mesh, etc.)
- Resource strings (Get_String)
