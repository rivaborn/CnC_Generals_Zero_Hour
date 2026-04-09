# Generals/Code/Tools/WorldBuilder/src/EditCoordParameter.cpp

## Purpose
Handles user input for editing 3D coordinate parameters in the WorldBuilder tool.

## Responsibilities
- Displays current 3D coordinates in dialog controls
- Validates and updates coordinates when user submits changes
- Shows error feedback for invalid input
- Manages dialog lifecycle (init, OK, cancel)

## Key Types
- EditCoordParameter (Class): Dialog for editing 3D coordinates
- Coord3D (Not inferable): 3D coordinate structure
- Real (Type): Floating-point number type

## Key Functions
### EditCoordParameter::OnInitDialog
- Purpose: Initializes dialog with current coordinate values
- Calls: CDialog::OnInitDialog, m_parameter->getCoord3D, CEdit::SetWindowText

### EditCoordParameter::OnOK
- Purpose: Validates and applies new coordinate values
- Calls: CEdit::GetWindowText, sscanf, m_parameter->friend_setCoord3D, CDialog::OnOK, MessageBeep

## Globals
None

## Dependencies
- stdafx.h, worldbuilder.h, EditCoordParameter.h
- GameLogic/Scripts.h, GameLogic/SidesList.h, GameLogic/PolygonTrigger.h
- MFC classes (CDialog, CEdit, CString)
- Windows API (MessageBeep)
