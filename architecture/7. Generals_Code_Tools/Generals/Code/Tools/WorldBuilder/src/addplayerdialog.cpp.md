# Generals/Code/Tools/WorldBuilder/src/addplayerdialog.cpp

## Purpose
Handles the UI dialog for adding a player to the WorldBuilder tool.

## Responsibilities
- Manages the AddPlayerDialog UI
- Populates faction combo box with available player templates
- Validates and adds selected player to the game
- Handles undo/redo operations for player addition

## Key Types
- AddPlayerDialog (class): Dialog for adding players
- PlayerTemplate (struct): Represents a player template
- SidesList (class): Manages list of game sides/players

## Key Functions
### AddPlayerDialog::OnOK
- Purpose: Handles dialog confirmation and adds selected player
- Calls: GetDlgItem, GetLBText, GetWindowText, findPlayerTemplate, addPlayerByTemplate, validateSides, AddAndDoUndoable

### AddPlayerDialog::OnInitDialog
- Purpose: Initializes the dialog and populates faction combo box
- Calls: ResetContent, getPlayerTemplateCount, getNthPlayerTemplate, AddString, SetCurSel

### AddPlayerDialog::OnCancel
- Purpose: Handles dialog cancellation
- Calls: clear

## Globals
- ThePlayerTemplateStore (PlayerTemplateStore*): Global player template store
- TheSidesList (SidesList*): Global sides list

## Dependencies
- stdafx.h, worldbuilder.h, addplayerdialog.h
- Common/WellKnownKeys.h, Common/PlayerTemplate.h
- GameLogic/SidesList.h, WorldBuilderDoc.h, CUndoable.h
- MFC classes (CDialog, CComboBox, CString)
- AsciiString, Bool, REF_PTR_RELEASE
