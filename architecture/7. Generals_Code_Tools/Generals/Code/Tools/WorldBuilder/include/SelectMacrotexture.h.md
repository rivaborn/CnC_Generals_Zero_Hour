# Generals/Code/Tools/WorldBuilder/include/SelectMacrotexture.h

## Purpose
Header file for the `SelectMacrotexture` dialog class used in WorldBuilder to select macro textures.

## Responsibilities
- Defines the `SelectMacrotexture` dialog class.
- Declares member variables and methods for texture selection UI.
- Manages a tree view control for displaying textures.
- Handles dialog initialization and data exchange.

## Key Types
- **SelectMacrotexture (Class)**: Dialog for selecting macro textures in WorldBuilder.
- **(anonymous enum) (Enum)**: Contains `IDD` enum value for dialog resource ID.
- **IDD (Enum)**: Dialog resource identifier (`IDD_MACRO_TEXTURE`).

## Key Functions
### SelectMacrotexture/SelectMacrotexture
- Purpose: Constructor for the `SelectMacrotexture` dialog.
- Calls: None.

### SelectMacrotexture/DoDataExchange
- Purpose: Handles data exchange between dialog controls and member variables.
- Calls: None.

### SelectMacrotexture/OnNotify
- Purpose: Processes notification messages from the dialog.
- Calls: None.

### SelectMacrotexture/OnInitDialog
- Purpose: Initializes the dialog when it is created.
- Calls: None.

### SelectMacrotexture/DECLARE_MESSAGE_MAP
- Purpose: Declares the message map for the dialog class.
- Calls: None.

## Globals
- None.

## Dependencies
- `CDialog`, `CWnd`, `CDataExchange`, `CTreeCtrl` (MFC classes).
- `DECLARE_MESSAGE_MAP()` (MFC macro).
- `IDD_MACRO_TEXTURE` (resource ID).
