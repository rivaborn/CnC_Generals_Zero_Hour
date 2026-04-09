# Generals/Code/Tools/WW3D/max2w3d/GameMtlPassDlg.cpp

## Purpose
Manages the dialog interface for editing material passes in the Max2W3D exporter tool.

## Responsibilities
- Handles dialog creation and message processing for material pass editing
- Manages sub-dialogs for different material properties (vertex, shader, texture)
- Maintains tabbed interface for navigating between material property pages
- Synchronizes material data between the UI and the underlying GameMtl object

## Key Types
- `GameMtlPassDlg` (Class): Main dialog class for material pass editing
- `PassDlgProc` (Function): Dialog procedure that routes messages to GameMtlPassDlg
- `_Pass_Index_To_Flag` (Array): Maps pass indices to material flags

## Key Functions
### `PassDlgProc`
- Purpose: Routes Windows messages to the appropriate GameMtlPassDlg instance
- Calls: `GameMtlPassDlg::DialogProc`

### `GameMtlPassDlg::DialogProc`
- Purpose: Handles Windows messages for the material pass dialog
- Calls: `GameMtlVertexMaterialDlg`, `GameMtlShaderDlg`, `PS2GameMtlShaderDlg`, `GameMtlTextureDlg` constructors, `TabCtrl_InsertItem`, `TabCtrl_AdjustRect`, `TabCtrl_SetCurSel`

### `GameMtlPassDlg::ReloadDialog`
- Purpose: Updates all controls with current material data
- Calls: `TheMtl->Update`, `Page[i]->ReloadDialog`

### `GameMtlPassDlg::SetThing`
- Purpose: Sets the material being edited
- Calls: `Page[i]->SetThing`

## Globals
- `_Pass_Index_To_Flag` (int[]): Maps pass indices to material rollup flags

## Dependencies
- `GameMtlPassDlg.h`, `dllmain.h`, `resource.h`, `GameMtl.h`, `GameMtlDlg.h`, `GameMtlShaderDlg.h`, `PS2GameMtlShaderDlg.h`, `GameMtlTextureDlg.h`, `GameMtlVertexMaterialDlg.h`, `w3d_file.h`
- `IMtlParams`, `GameMtl`, `ReferenceTarget` classes
- Windows API functions (HWND, WM_*, TabCtrl_*, etc.)
