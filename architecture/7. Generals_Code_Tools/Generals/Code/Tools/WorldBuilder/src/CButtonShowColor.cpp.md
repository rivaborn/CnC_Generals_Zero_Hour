# Generals/Code/Tools/WorldBuilder/src/CButtonShowColor.cpp

## Purpose
Handles rendering and color conversion for a button that displays a color in the WorldBuilder tool.

## Responsibilities
- Renders a colored button using GDI
- Converts between RGB and BGR color formats
- Manages button destruction
- Handles paint messages via MFC message map

## Key Types
- CButtonShowColor (Class): Custom button class for color display
- CColor (Type): Stores the color value (external)

## Key Functions
### OnPaint
- Purpose: Renders the button with the current color
- Calls: CPaintDC constructor, CPen constructor, CBrush constructor, GetWindowRect, ScreenToClient, FillRect, MoveTo, LineTo, SelectObject

### RGBtoBGR
- Purpose: Converts RGB color format to BGR
- Calls: None

### BGRtoRGB
- Purpose: Converts BGR color format to RGB
- Calls: RGBtoBGR

## Globals
- None

## Dependencies
- StdAfx.h (precompiled header)
- Gameclient/ParticleSys.h (not directly used here)
- CButtonShowColor.h (header)
- MFC classes: CPaintDC, CPen, CBrush, CRect, CButton
- Windows API: DestroyWindow, RGB macro
