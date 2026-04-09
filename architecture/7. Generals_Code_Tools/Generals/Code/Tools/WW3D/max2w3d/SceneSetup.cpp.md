# Generals/Code/Tools/WW3D/max2w3d/SceneSetup.cpp

## Purpose
Implements the MAXScript function `wwSceneSetup` to display a dialog for configuring LOD and damage model parameters in 3D Studio Max.

## Responsibilities
- Exposes `wwSceneSetup` as a MAXScript primitive
- Parses input array parameters for LOD/damage model settings
- Displays a modal dialog for user input
- Returns updated parameters as an array

## Key Types
- `SceneSetupDlg` (Class): Dialog class for user input (defined in SceneSetupDlg.h)

## Key Functions
### `scene_setup_cf`
- Purpose: Handles MAXScript `wwSceneSetup` function call
- Calls:
  - `check_arg_count`
  - `type_check`
  - `Array::get`
  - `Integer::intern`
  - `Float::intern`
  - `SceneSetupDlg::DoModal`
  - `Array::append`
  - `return_value`

## Globals
- `def_visible_primitive` (macro): Registers `scene_setup` as a visible MAXScript primitive

## Dependencies
- `SceneSetupDlg.h`
- `<MaxScrpt.h>`
- `<Numbers.h>`
- `<Arrays.h>`
- `<definsfn.h>`
- MAXScript interface functions (`check_arg_count`, `type_check`, etc.)
