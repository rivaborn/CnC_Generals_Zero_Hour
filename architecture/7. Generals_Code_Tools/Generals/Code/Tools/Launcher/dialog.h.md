# Generals/Code/Tools/Launcher/dialog.h

## Purpose
Header file declaring a patch dialog creation function and its associated window handle.

## Responsibilities
- Declares the `Create_Patch_Dialog` function.
- Declares the global `PatchDialog` window handle.
- Includes necessary Windows API headers.

## Key Types
- None

## Key Functions
### Create_Patch_Dialog
- Purpose: Creates and returns a handle to the patch dialog window.
- Calls: Not inferable (implementation not shown).

## Globals
- PatchDialog (HWND): Stores the handle to the patch dialog window.

## Dependencies
- `winblows.h`: Custom Windows API wrapper.
- `<commctrl.h>`: Windows Common Controls header.
- `HWND`: Windows API type (handle to window).
