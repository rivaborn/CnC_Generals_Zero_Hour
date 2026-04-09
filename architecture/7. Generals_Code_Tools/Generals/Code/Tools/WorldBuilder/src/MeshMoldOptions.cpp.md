# Generals/Code/Tools/WorldBuilder/src/MeshMoldOptions.cpp

## Purpose
Handles the UI and logic for mesh molding options in the WorldBuilder editor.

## Responsibilities
- Manages dialog UI for mesh molding parameters (height, scale, angle)
- Handles file selection for .w3d mesh models
- Coordinates with MeshMoldTool for preview and application
- Maintains state for raise/lower operations

## Key Types
- MeshMoldOptions (Class): Main dialog class for mesh molding options
- None: No other significant types defined

## Key Functions
### MeshMoldOptions::OnInitDialog
- Purpose: Initializes the dialog UI and loads available .w3d files
- Calls: COptionsPanel::OnInitDialog, TheFileSystem->getFileListInDirectory

### MeshMoldOptions::setHeight/setScale/setAngle
- Purpose: Updates the current height/scale/angle values and UI
- Calls: MeshMoldTool::updateMeshLocation

### MeshMoldOptions::PopSliderChanged
- Purpose: Handles slider value changes for height, scale, and angle
- Calls: MeshMoldTool::updateMeshLocation

### MeshMoldOptions::OnPreview/OnApplyMesh
- Purpose: Toggles preview mode or applies the mesh molding
- Calls: MeshMoldTool::updateMeshLocation, MeshMoldTool::apply

### MeshMoldOptions::OnNotify
- Purpose: Handles tree view selection changes for mesh model selection
- Calls: MeshMoldTool::updateMeshLocation

## Globals
- m_currentHeight (Real): Current height value for mesh molding
- m_currentScale (Real): Current scale value for mesh molding
- m_currentAngle (Int): Current angle value for mesh molding
- m_staticThis (MeshMoldOptions*): Pointer to the dialog instance
- m_doingPreview (Bool): Flag indicating if preview mode is active
- m_raiseOnly/m_lowerOnly (Bool): Flags for raise/lower operations

## Dependencies
- "stdafx.h", "worldbuilder.h", "worldbuilderDoc.h", "MeshMoldOptions.h", "Common/FileSystem.h"
- COptionsPanel, CWnd, CButton, CRect, CString, FilenameList, AsciiString, TheFileSystem, MeshMoldTool, CWorldBuilderDoc
