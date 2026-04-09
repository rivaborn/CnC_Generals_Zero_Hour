# Generals/Code/Tools/ImagePacker/Source/Window Procedures/PreviewProc.cpp

## Purpose
Handles the preview window for the ImagePacker tool, rendering texture pages and updating the display.

## Responsibilities
- Processes WM_PAINT messages to render texture previews
- Creates and manages the preview window
- Updates window title and dimensions based on current texture page

## Key Types
- None

## Key Functions
### PreviewProc
- Purpose: Window procedure for handling preview window messages
- Calls: `BeginPaint`, `GetStockObject`, `SelectObject`, `CreatePen`, `MoveToEx`, `LineTo`, `DeleteObject`, `FillRect`, `EndPaint`, `DefWindowProc`

### MakePreviewDisplay
- Purpose: Creates and registers the preview window
- Calls: `RegisterClassEx`, `CreateWindowEx`, `ShowWindow`

### UpdatePreviewWindow
- Purpose: Updates preview window title, size, and invalidates for redraw
- Calls: `SetWindowText`, `ClientToScreen`, `AdjustWindowRect`, `MoveWindow`, `InvalidateRect`

## Globals
- None

## Dependencies
- `<windows.h>` for Win32 API
- `<stdio.h>` for `sprintf`
- `ImagePacker.h` for `TheImagePacker`, `TexturePage`, `ImageInfo`
- `WinMain.h` for `ApplicationHInstance`
