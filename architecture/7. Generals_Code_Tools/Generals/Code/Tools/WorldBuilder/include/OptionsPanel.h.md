# Generals/Code/Tools/WorldBuilder/include/OptionsPanel.h

## Purpose
Header file for the COptionsPanel dialog class, part of the WorldBuilder tool's UI system.

## Responsibilities
- Defines the COptionsPanel dialog class
- Declares message handlers for undo/redo operations
- Manages dialog data exchange
- Handles window movement events

## Key Types
- COptionsPanel (Class): Dialog class for options panel in WorldBuilder
- (anonymous enum) (Enum): Contains IDD_NO_OPTIONS identifier
- IDD (Enum): Dialog resource identifier

## Key Functions
### COptionsPanel::DoDataExchange
- Purpose: Handles dialog data exchange
- Calls: CDataExchange methods

### COptionsPanel::OnMove
- Purpose: Handles window movement events
- Calls: None

### COptionsPanel::OnEditRedo
- Purpose: Handles redo operation command
- Calls: None

### COptionsPanel::OnUpdateEditRedo
- Purpose: Updates redo command UI state
- Calls: None

### COptionsPanel::OnEditUndo
- Purpose: Handles undo operation command
- Calls: None

### COptionsPanel::OnUpdateEditUndo
- Purpose: Updates undo command UI state
- Calls: None

## Globals
- OPTIONS_PANEL_SECTION (String): Section name for options window settings

## Dependencies
- "resource.h" for resource definitions
- CDialog, CWnd, CDataExchange, CCmdUI from MFC
- DECLARE_MESSAGE_MAP() macro
