# Generals/Code/Tools/ImagePacker/Source/Window Procedures/PageErrorProc.cpp

## Purpose
Handles the error dialog window procedure for texture page processing failures in the ImagePacker tool.

## Responsibilities
- Displays a list of failed texture pages and their error reasons
- Processes user input (OK button) to close the dialog
- Initializes the dialog with error information from TheImagePacker

## Key Types
- None

## Key Functions
### PageErrorProc
- Purpose: Dialog procedure for error window handling
- Calls: `GetDlgItem`, `SendMessage`, `BitTest`, `TheImagePacker->getFirstTexturePage`, `TheImagePacker->getOutputFile`, `EndDialog`

## Globals
- TheImagePacker (TexturePacker*): Global instance of the image packer tool

## Dependencies
- `<windows.h>` for Windows API functions
- `<stdio.h>` for sprintf
- "ImagePacker.h" for TexturePacker and TexturePage classes
- "Resource.h" for dialog control IDs
