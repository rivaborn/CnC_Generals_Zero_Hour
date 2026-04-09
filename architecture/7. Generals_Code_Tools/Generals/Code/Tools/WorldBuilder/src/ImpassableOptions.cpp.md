# Generals/Code/Tools/WorldBuilder/src/ImpassableOptions.cpp

## Purpose
Handles UI for configuring impassable slope angles in WorldBuilder.

## Responsibilities
- Manages a dialog for setting slope thresholds
- Validates slope input (0-90 degrees)
- Updates terrain rendering to show impassable areas
- Handles preview updates of the heightmap

## Key Types
- **ImpassableOptions (class)**: Dialog for slope angle configuration

## Key Functions
### ImpassableOptions::ImpassableOptions
- Purpose: Constructor initializes dialog and terrain rendering
- Calls: TheTerrainRenderObject->getShowImpassableAreas, setShowImpassableAreas

### ImpassableOptions::ValidateSlope
- Purpose: Validates slope angle is within 0-90 degree range
- Calls: None

### ImpassableOptions::OnInitDialog
- Purpose: Initializes dialog controls with current slope value
- Calls: GetDlgItem, SetWindowText, CDialog::OnInitDialog

### ImpassableOptions::OnAngleChange
- Purpose: Handles slope value changes from UI input
- Calls: GetDlgItem, GetWindowText, ValidateSlope, setViewImpassableAreaSlope

### ImpassableOptions::OnPreview
- Purpose: Updates heightmap preview in 3D view
- Calls: CWorldBuilderDoc::GetActive3DView, updateHeightMapInView

## Globals
- **m_slopeToShow (Real)**: Current slope angle being edited
- **m_defaultSlopeToShow (Real)**: Original slope value
- **m_showImpassableAreas (Bool)**: Previous impassable area visibility state

## Dependencies
- "StdAfx.h", "resource.h", "ImpassableOptions.h"
- TheTerrainRenderObject (external
