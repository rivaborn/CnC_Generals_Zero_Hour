# Generals/Code/Tools/WW3D/max2w3d/GameMtlDlg.h

## Purpose
Defines the `GameMtlDlg` class, a dialog interface for editing `GameMtl` materials in the 3DS Max material editor.

## Responsibilities
- Manages the UI for material editing in 3DS Max
- Handles material parameter updates and validation
- Controls pass count and surface type panels
- Manages displacement map settings
- Provides access to the underlying `GameMtl` object

## Key Types
- **GameMtlDlg (Class)**: Dialog interface for material editing
- **GameMtlPassDlg (Class)**: Reference to pass-specific dialog (forward declared)
- **GameMtl (Class)**: Reference to the material being edited (forward declared)
- **(anonymous enum) (Enum)**: Defines `MAX_PASSES = 4`

## Key Functions
### GameMtlDlg()
- Purpose: Constructor for the material editor dialog
- Calls: Not inferable

### Build_Dialog()
- Purpose: Constructs the dialog UI components
- Calls: Not inferable

### DisplacementMapProc()
- Purpose: Handles displacement map panel messages
- Calls: Not inferable

### SurfaceTypeProc()
- Purpose: Handles surface type panel messages
- Calls: Not inferable

### PassCountProc()
- Purpose: Handles pass count panel messages
- Calls: Not inferable

### Set_Pass_Count_Dialog()
- Purpose: Updates the pass count dialog UI
- Calls: Not inferable

## Globals
- **HwndEdit (HWND)**: Handle to the materials editor dialog
- **HwndPassCount (HWND)**: Handle to the pass count panel
- **HwndSurfaceType (HWND)**: Handle to the surface type panel
- **HwndDisplacement
