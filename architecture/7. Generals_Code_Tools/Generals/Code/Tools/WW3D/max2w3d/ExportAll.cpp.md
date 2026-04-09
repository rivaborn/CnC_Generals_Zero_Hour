# Generals/Code/Tools/WW3D/max2w3d/ExportAll.cpp

## Purpose
Implements a MAXScript function to present a dialog for users to select an export directory and toggle recursive export.

## Responsibilities
- Registers the `wwExportTreeSettings` MAXScript function
- Handles dialog input/output for export settings
- Validates and processes MAXScript array arguments
- Returns user-selected settings as a MAXScript array

## Key Types
- `ExportAllDlg` (Class): Dialog class for user input (external)
- `Value` (Type): MAXScript value type (external)
- `Array` (Type): MAXScript array type (external)
- `String` (Type): MAXScript string type (external)

## Key Functions
### `export_tree_settings_cf`
- Purpose: Processes MAXScript arguments, shows dialog, and returns user settings
- Calls: `check_arg_count`, `type_check`, `Array::get`, `String::to_string`, `ExportAllDlg::DoModal`, `Array::append`, `return_value`

## Globals
- `def_visible_primitive` (Macro): Registers MAXScript function (line 60)

## Dependencies
- `ExportAllDlg.h` (header)
- MAXScript API: `MaxScrpt.h`, `Arrays.h`, `Strings.h`, `definsfn.h`
- External symbols: `check_arg_count`, `type_check`, `MAXScript_interface`, `undefined`, `new Array`, `new String`, `true_value`, `false_value`
