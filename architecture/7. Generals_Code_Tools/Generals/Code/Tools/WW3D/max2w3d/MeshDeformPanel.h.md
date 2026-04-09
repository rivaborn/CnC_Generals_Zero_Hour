# Generals/Code/Tools/WW3D/max2w3d/MeshDeformPanel.h

## Purpose
Header file defining the MeshDeformPanelClass for mesh deformation UI in the 3DS Max plugin.

## Responsibilities
- Manages UI controls for mesh deformation panel
- Handles vertex color and deformation state updates
- Provides accessors for deformation settings
- Processes Windows messages and commands for the panel

## Key Types
- MeshDeformClass (Class): Forward declaration for mesh deformer object
- MeshDeformPanelClass (Class): Main panel class handling deformation UI

## Key Functions
### MeshDeformPanelClass::Set_Deformer
- Purpose: Assigns a mesh deformer object to the panel
- Calls: None

### MeshDeformPanelClass::Set_Current_Set
- Purpose: Sets the current deformation set
- Calls: None

### MeshDeformPanelClass::Set_Max_Sets
- Purpose: Sets the maximum number of deformation sets
- Calls: None

### MeshDeformPanelClass::Set_Current_State
- Purpose: Sets the current deformation state
- Calls: None

### MeshDeformPanelClass::Update_Vertex_Color
- Purpose: Updates the vertex color display
- Calls: None

### MeshDeformPanelClass::On_Message
- Purpose: Handles Windows messages for the panel
- Calls: None

### MeshDeformPanelClass::On_Command
- Purpose: Processes command messages for the panel
- Calls: None

## Globals
- None

## Dependencies
- `<Max.h>`: 3DS Max SDK headers
- `"Resource.H"`: Local resource definitions
- `IColorSwatch`, `ICustEdit`, `ISpinnerControl`, `ICustButton`: 3DS Max UI control interfaces
- Windows API (`HW
