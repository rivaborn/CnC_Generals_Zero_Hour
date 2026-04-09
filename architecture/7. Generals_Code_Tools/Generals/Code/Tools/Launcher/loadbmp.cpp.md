# Generals/Code/Tools/Launcher/loadbmp.cpp

## Purpose
Handles loading and displaying BMP bitmap files in a Windows application.

## Responsibilities
- Loads BMP files from disk
- Creates device-independent bitmaps and palettes
- Renders bitmaps to a window
- Manages GDI resources (bitmaps, palettes, DCs)

## Key Types
- LoadBmp (Class): wrapper for BMP loading and rendering
- BITMAPFILEHEADER (Struct): BMP file header
- BITMAPINFOHEADER (Struct): BMP info header

## Key Functions
### LoadBmp::init
- Purpose: Loads a BMP file and prepares it for display
- Calls: CreateFile, ReadFile, GlobalAlloc, CreatePalette, CreateDIBitmap, GetDC, SelectPalette, RealizePalette, ReleaseDC, InvalidateRect, UpdateWindow

### LoadBmp::drawBmp
- Purpose: Renders the loaded bitmap to the window
- Calls: InvalidateRect, BeginPaint, SelectPalette, RealizePalette, CreateCompatibleDC, SelectObject, GetObject, GetClientRect, SetStretchBltMode, StretchBlt, DeleteDC, EndPaint

## Globals
- None

## Dependencies
- Windows GDI functions (CreateFile, ReadFile, CreatePalette, etc.)
- Windows data structures (BITMAPFILEHEADER, BITMAPINFOHEADER, LOGPALETTE, etc.)
- loadbmp.h header file
