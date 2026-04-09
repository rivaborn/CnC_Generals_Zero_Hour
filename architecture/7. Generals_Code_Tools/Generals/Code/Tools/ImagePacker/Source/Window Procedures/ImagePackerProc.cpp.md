# Generals/Code/Tools/ImagePacker/Source/Window Procedures/ImagePackerProc.cpp

## Purpose
Handles the main dialog window procedure for the ImagePacker tool, managing UI interactions and program flow.

## Responsibilities
- Processes Windows messages for the main dialog
- Manages UI state and updates based on user input
- Coordinates with TheImagePacker instance for core functionality
- Handles preview window creation/destruction
- Validates and applies user settings

## Key Types
- None

## Key Functions
### ImagePackerProc
- Purpose: Main dialog procedure handling WM_INITDIALOG and WM_COMMAND messages
- Calls: TheImagePacker methods (setWindowHandle, statusMessage, getGutter, getOutputAlpha, etc.), UpdatePreviewWindow(), MakePreviewDisplay(), DirectorySelectProc, GetSystemMetrics, MoveWindow, SetDlgItemInt, CheckDlgButton, SetDlgItemText, SendDlgItemMessage, IsDlgButtonChecked, EnableWindow, GetDlgItem, SendMessage, MessageBox, EndDialog, DialogBox

## Globals
- TheImagePacker (ImagePacker*): Main application instance

## Dependencies
- Windows.h, io.h
- ImagePacker.h, Resource.h, WindowProc.h, WinMain.h
- External symbols: UpdatePreviewWindow(), MakePreviewDisplay(), DirectorySelectProc, ApplicationHInstance, MAX_OUTPUT_FILE_LEN, DIRECTORY_SELECT_DIALOG, and various resource IDs (BUTTON_PREVIOUS, EDIT_GUTTER, etc.)
