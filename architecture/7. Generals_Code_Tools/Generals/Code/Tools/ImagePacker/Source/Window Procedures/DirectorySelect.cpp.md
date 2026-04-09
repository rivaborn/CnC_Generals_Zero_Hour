# Generals/Code/Tools/ImagePacker/Source/Window Procedures/DirectorySelect.cpp

## Purpose
Handles directory selection dialog for the ImagePacker tool, allowing users to browse and select folders.

## Responsibilities
- Manages directory browsing UI with drive selection and folder listing
- Handles user interactions (add/cancel buttons, double-click navigation)
- Maintains current directory state and validates selections
- Prevents duplicate folder additions

## Key Types
- None

## Key Functions
### selectDrive
- Purpose: Selects the current drive in the combo box based on working directory
- Calls: GetCurrentDirectory, SendDlgItemMessage, sprintf

### DirectorySelectProc
- Purpose: Window procedure for directory selection dialog handling all messages
- Calls: GetCurrentDirectory, SendDlgItemMessage, SetDlgItemText, SetCurrentDirectory, MessageBox, EndDialog, EnableWindow, sprintf, strcmp, strlen, strcat

## Globals
- startDir (char[_MAX_PATH]): Stores initial directory for restoration

## Dependencies
- Windows.h, stdio.h
- ImagePacker.h, Resource.h
- Uses TheImagePacker global instance for main window handle
