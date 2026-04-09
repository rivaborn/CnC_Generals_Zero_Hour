# Generals/Code/Tools/Launcher/dialog.cpp

## Purpose
Creates and manages a dialog window displayed during the game patching process.

## Responsibilities
- Creates the patch progress dialog window
- Handles dialog messages (initialization, painting, commands, closing)
- Manages a progress bar and splash image during patching

## Key Types
- None

## Key Functions
### Create_Patch_Dialog
- Purpose: Creates and displays the patch progress dialog
- Calls: CreateDialog, ShowWindow, SetForegroundWindow

### Patch_Window_Proc
- Purpose: Handles window messages for the patch dialog
- Calls: SendMessage, LoadBmp::init, LoadBmp::drawBmp, DestroyWindow, PostQuitMessage, exit

## Globals
- PatchDialog (HWND): Stores the handle to the patch dialog window

## Dependencies
- winblows.h, resource.h, loadbmp.h, commctrl.h
- Global_instance (external variable)
- LoadBmp class (external)
- Windows API functions (CreateDialog, ShowWindow, etc.)
