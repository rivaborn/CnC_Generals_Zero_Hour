# Generals/Code/Tools/WorldBuilder/src/EditGroup.cpp

## Purpose
Handles the UI dialog for editing script groups in WorldBuilder.

## Responsibilities
- Manages the EditGroup dialog class
- Syncs UI controls with ScriptGroup properties
- Handles user input for group name, active state, and subroutine flag

## Key Types
- `EditGroup` (class): Dialog for editing script groups
- `ScriptGroup` (pointer): Reference to the group being edited

## Key Functions
### `EditGroup::OnOK`
- Purpose: Saves user input back to the ScriptGroup
- Calls: `m_scriptGroup->setName`, `m_scriptGroup->setActive`, `m_scriptGroup->setSubroutine`, `CDialog::OnOK`

### `EditGroup::OnInitDialog`
- Purpose: Initializes dialog controls with ScriptGroup data
- Calls: `CDialog::OnInitDialog`, `GetDlgItem`, `SetCheck`, `SetWindowText`

## Globals
None

## Dependencies
- `stdafx.h`, `worldbuilder.h`, `EditGroup.h`, `GameLogic/Scripts.h`
- MFC classes: `CDialog`, `CWnd`, `CButton`, `CEdit`, `CDataExchange`, `CString`
- `AsciiString` type from external code
