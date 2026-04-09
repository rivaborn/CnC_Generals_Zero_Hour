# Generals/Code/Tools/WW3D/max2w3d/MeshDeformPanel.cpp

## Purpose
Handles the UI panel for mesh deformation operations in the 3DS Max plugin.

## Responsibilities
- Manages dialog messages and UI controls for mesh deformation
- Coordinates with the MeshDeformClass to apply vertex color changes
- Updates UI elements based on deformation state and parameters
- Handles slider, button, and color swatch interactions

## Key Types
- MeshDeformPanelClass (Class): Main panel controller for mesh deformation UI
- VertColor (Struct): Vertex color data structure (external)

## Key Functions
### Message_Proc
- Purpose: Windows message handler for the dialog panel
- Calls: Get_Object, On_Message, SetProp, RemoveProp, SAFE_DELETE

### On_Message
- Purpose: Processes Windows messages for the panel
- Calls: GetIColorSwatch, GetICustEdit, GetISpinner, GetICustButton, Set_Max_Sets, Set_Current_Set, On_Command, Update_Vertex_Color

### Set_Deformer
- Purpose: Links the panel to a MeshDeformClass instance
- Calls: Get_Deform_State, Update_Vertex_Color

### Update_Vertex_Color
- Purpose: Synchronizes the color swatch with the deformer's vertex color
- Calls: Get_Vertex_Color, SetColor

### Set_Max_Sets
- Purpose: Updates the maximum deformation sets and notifies the deformer
- Calls: Set_Max_Deform_Sets

### Set_Current_Set
- Purpose: Updates the current deformation set and notifies the deformer
- Calls: Set_Current_Set

## Globals
- PANEL_OBJ_PROP (const char*): Property name for storing panel object in window
- WINAPI (macro): Windows API calling convention

## Dependencies
- MeshDeformPanel.H, Resource.H, Util.H, MeshDeform.H
- Windows API (HWND, WPARAM, LPARAM, etc.)
- 3DS Max SDK interfaces (IColorSwatch, ICustEdit, ISpinner, ICustButton)
