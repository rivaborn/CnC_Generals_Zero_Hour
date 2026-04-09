# Generals/Code/Tools/WW3D/max2w3d/vxldbg.cpp

## Purpose
Implements a voxel debugging window for visualizing voxel data in a 3D modeling tool.

## Responsibilities
- Creates and manages a dialog window for voxel inspection
- Renders voxel layers as a bitmap preview
- Handles user interaction via spinner control for layer selection
- Manages the voxel palette and display updates

## Key Types
- `VoxelDebugWindowClass` (Class): Main debug window manager for voxel data
- `PaletteClass` (Class): Color palette for voxel rendering
- `_VoxelPalette` (Static): Global palette instance for voxel colors

## Key Functions
### `VoxelDebugWindowClass::Dialog_Proc`
- Purpose: Handles dialog messages and user input
- Calls: `GetDlgItem`, `SetupIntSpinner`, `update_display`, `EndDialog`

### `VoxelDebugWindowClass::update_display`
- Purpose: Renders current voxel layer to the bitmap display
- Calls: `Bitmap->Clear`, `Voxel->Is_Solid`, `Bitmap->Set_Pixel`, `StretchBlt`

### `_dialog_proc`
- Purpose: Static callback that routes messages to the window instance
- Calls: `window->Dialog_Proc`

## Globals
- `_VoxelPalette` (PaletteClass): Stores the two-color palette for voxel rendering

## Dependencies
- `vxldbg.h`, `resource.h`, `dllmain.h`
- Windows API: `DialogBoxParam`, `GetDlgItem`, `GetClientRect`, `BitBlt`, `StretchBlt`
- Custom classes: `SimpleDIBClass`, `VoxelClass`, spinner control functions
