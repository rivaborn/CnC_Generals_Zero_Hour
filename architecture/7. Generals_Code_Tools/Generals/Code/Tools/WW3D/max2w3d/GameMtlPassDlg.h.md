# Generals/Code/Tools/WW3D/max2w3d/GameMtlPassDlg.h

## Purpose
Defines the `GameMtlPassDlg` class, a dialog for editing material passes in the Max2W3d tool.

## Responsibilities
- Manages a tabbed dialog for editing material parameters (vertex, shader, texture)
- Handles material parameter updates and display
- Provides interface to the material editor
- Manages dialog activation and validation

## Key Types
- **GameMtlPassDlg (Class)**: Material pass editing dialog
- **GameMtlFormClass (Class)**: Form class for material editing pages
- **GameMtl (Class)**: Material being edited
- **PAGE_COUNT (Enum)**: Number of editing pages (3)

## Key Functions
### GameMtlPassDlg()
- Purpose: Constructor for the material pass dialog
- Calls: Not inferable

### DialogProc()
- Purpose: Handles dialog messages
- Calls: Not inferable

### Invalidate()
- Purpose: Invalidates the dialog
- Calls: Not inferable

### ReloadDialog()
- Purpose: Reloads the dialog contents
- Calls: Not inferable

### SetThing()
- Purpose: Sets the material being edited
- Calls: Not inferable

### SetTime()
- Purpose: Sets the current time for animation
- Calls: Not inferable

### ActivateDlg()
- Purpose: Activates/deactivates the dialog
- Calls: Not inferable

## Globals
- **IParams (IMtlParams*)**: Interface to the material editor
- **TheMtl (GameMtl*)**: Current material being edited
- **HwndEdit (HWND)**: Window handle of the materials editor dialog
- **HwndPanel (HWND)**: Rollup parameters panel window handle
- **PassIndex (
