# Generals/Code/Tools/GUIEdit/Source/Dialog Procedures/NewLayoutDialog.cpp

## Purpose
Handles the dialog procedure for creating a new layout in the GUI editor.

## Responsibilities
- Initializes the new layout dialog
- Processes user input (OK/Cancel/Close)
- Triggers new layout creation via TheEditor

## Key Types
None

## Key Functions
### initNewLayoutDialog
- Purpose: Sets default keyboard focus to the OK button
- Calls: SetFocus, GetDlgItem

### NewLayoutDialogProc
- Purpose: Main dialog procedure for new layout creation
- Calls: initNewLayoutDialog, TheEditor->newLayout, EndDialog

## Globals
- TheEditor (EditWindow*): Global editor instance

## Dependencies
- Windows.h (HWND, WPARAM, LPARAM, etc.)
- BaseType.h (basic types)
- Resource.h (dialog IDs)
- EditWindow.h (TheEditor)
- GUIEdit.h (editor context)
