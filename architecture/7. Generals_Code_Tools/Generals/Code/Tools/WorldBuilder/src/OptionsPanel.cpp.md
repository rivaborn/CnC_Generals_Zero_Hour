# Generals/Code/Tools/WorldBuilder/src/OptionsPanel.cpp

## Purpose
Implements the COptionsPanel dialog class for the WorldBuilder tool, handling UI events and window management.

## Responsibilities
- Manages dialog creation and data exchange
- Handles window movement and position persistence
- Delegates undo/redo operations to the document
- Manages command UI updates for undo/redo

## Key Types
- COptionsPanel (Class): Main dialog class for options panel

## Key Functions
### COptionsPanel::COptionsPanel
- Purpose: Constructor for the options panel dialog
- Calls: CDialog constructor

### COptionsPanel::OnMove
- Purpose: Handles window movement and saves position to config
- Calls: CDialog::OnMove, CRect::GetWindowRect, AfxGetApp()->WriteProfileInt

### COptionsPanel::OnEditRedo
- Purpose: Delegates redo operation to the active document
- Calls: CWorldBuilderDoc::GetActiveDoc(), CWorldBuilderDoc::OnEditRedo

### COptionsPanel::OnUpdateEditRedo
- Purpose: Updates UI state for redo command
- Calls: CWorldBuilderDoc::GetActiveDoc(), CWorldBuilderDoc::OnUpdateEditRedo

### COptionsPanel::OnEditUndo
- Purpose: Delegates undo operation to the active document
- Calls: CWorldBuilderDoc::GetActiveDoc(), CWorldBuilderDoc::OnEditUndo

### COptionsPanel::OnUpdateEditUndo
- Purpose: Updates UI state for undo command
- Calls: CWorldBuilderDoc::GetActiveDoc(), CWorldBuilderDoc::OnUpdateEditUndo

## Globals
- OPTIONS_PANEL_SECTION (Not inferable): Used as config section name

## Dependencies
- stdafx.h, worldbuilder.h, worldbuilderdoc
