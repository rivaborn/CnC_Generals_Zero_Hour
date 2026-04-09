# Generals/Code/Tools/ImagePacker/Source/Window Procedures/ImageErrorProc.cpp

## Purpose
Handles the error dialog window procedure for the ImagePacker tool, displaying images that failed processing and their error reasons.

## Responsibilities
- Displays unprocessable images in a listbox with error reasons
- Handles user input (Proceed/Cancel buttons)
- Manages dialog initialization and message routing

## Key Types
- None

## Key Functions
### ImageErrorProc
- Purpose: Dialog procedure for error window
- Calls: `TheImagePacker->getImageCount()`, `TheImagePacker->getImage()`, `SendMessage()`, `EndDialog()`

## Globals
- `TheImagePacker` (ImagePacker*): Global instance of the image packer tool

## Dependencies
- `<windows.h>` for Windows API
- `<stdio.h>` for sprintf
- "ImagePacker.h" for ImagePacker class
- "Resource.h" for dialog controls (LIST_IMAGES, BUTTON_PROCEED, BUTTON_CANCEL)
