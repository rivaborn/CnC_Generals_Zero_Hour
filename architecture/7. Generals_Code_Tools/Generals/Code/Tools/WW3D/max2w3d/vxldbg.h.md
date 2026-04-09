# Generals/Code/Tools/WW3D/max2w3d/vxldbg.h

## Purpose
Header file defining a voxel debugging window class for the max2w3d tool.

## Responsibilities
- Declares `VoxelDebugWindowClass` for voxel visualization
- Manages voxel layer display and interaction
- Handles Windows dialog procedures for the debug UI
- Provides bitmap rendering of voxel data

## Key Types
- **VoxelDebugWindowClass (Class)**: Manages a debug window for voxel inspection.

## Key Functions
### VoxelDebugWindowClass::VoxelDebugWindowClass
- Purpose: Constructor initializing the debug window with a voxel object.
- Calls: Not inferable.

### VoxelDebugWindowClass::Display_Window
- Purpose: Displays the debug window.
- Calls: Not inferable.

### VoxelDebugWindowClass::Dialog_Proc
- Purpose: Handles Windows messages for the debug dialog.
- Calls: Not inferable.

### VoxelDebugWindowClass::update_display
- Purpose: Updates the displayed voxel layer.
- Calls: Not inferable.

## Globals
- None

## Dependencies
- `always.h`, `Max.h`, `simpdib.h`, `vxl.h`
- `SimpleDIBClass`, `VoxelClass`, `ISpinnerControl`, Windows API (`HWND`, `WPARAM`, `LPARAM`)
