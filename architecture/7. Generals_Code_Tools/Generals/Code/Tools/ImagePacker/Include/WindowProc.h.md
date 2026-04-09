# Generals/Code/Tools/ImagePacker/Include/WindowProc.h

## Purpose
Header file declaring dialog procedures for the ImagePacker utility.

## Responsibilities
- Declares window procedure callbacks for the ImagePacker tool
- Provides preview window creation and update functions
- Defines error dialog procedures for image and page errors
- Declares directory selection dialog procedure

## Key Types
None

## Key Functions
### ImagePackerProc
- Purpose: Main dialog procedure for the ImagePacker utility.
- Calls: Not inferable

### MakePreviewDisplay
- Purpose: Creates the preview display window.
- Calls: Not inferable

### UpdatePreviewWindow
- Purpose: Updates the preview window content.
- Calls: Not inferable

### PreviewProc
- Purpose: Window procedure for the preview display.
- Calls: Not inferable

### ImageErrorProc
- Purpose: Dialog procedure for image-related errors.
- Calls: Not inferable

### PageErrorProc
- Purpose: Dialog procedure for page-related errors.
- Calls: Not inferable

### DirectorySelectProc
- Purpose: Dialog procedure for directory selection.
- Calls: Not inferable

## Globals
None

## Dependencies
- Windows API (HWND, UINT, WPARAM, LPARAM, BOOL, CALLBACK)
- Standard C++ headers (not explicitly shown but implied by Windows API usage)
