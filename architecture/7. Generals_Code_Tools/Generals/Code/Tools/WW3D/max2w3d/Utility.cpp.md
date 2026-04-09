# Generals/Code/Tools/WW3D/max2w3d/Utility.cpp

## Purpose
Provides utility functions for MAXScript integration, including path resolution and user input dialogs.

## Responsibilities
- Exposes `wwGetAbsolutePath` to convert relative paths to absolute paths
- Exposes `wwInputBox` for user text input via a dialog
- Handles MAXScript function registration and argument validation

## Key Types
- `InputDlg` (Class): Dialog for text input

## Key Functions
### `get_absolute_path_cf`
- Purpose: Converts a relative path to an absolute path using a context directory
- Calls: `check_arg_count`, `type_check`, `Create_Full_Path`, `new String`, `return_value`

### `input_box_cf`
- Purpose: Displays a modal input dialog and returns user-entered text
- Calls: `key_arg`, `InputDlg::SetCaption`, `InputDlg::SetLabel`, `InputDlg::SetValue`, `InputDlg::DoModal`, `new String`, `return_value`

## Globals
- `def_visible_primitive` (Macro): Registers MAXScript functions (2 instances)

## Dependencies
- MAXScript API headers (`MaxScrpt.h`, `Arrays.h`, `Strings.h`, `definsfn.h`)
- Custom headers (`util.h`, `InputDlg.h`)
- External symbols: `Create_Full_Path`, `MAXScript_interface`, `unsupplied`, `undefined`
