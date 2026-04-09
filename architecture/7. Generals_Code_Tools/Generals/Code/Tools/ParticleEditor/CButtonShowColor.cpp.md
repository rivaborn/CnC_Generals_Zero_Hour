# Generals/Code/Tools/ParticleEditor/CButtonShowColor.cpp

## Purpose
This file implements a custom button control that displays a color preview in the Particle Editor tool.

## Responsibilities
- Renders a color preview in a button control
- Handles Windows message routing for painting
- Converts between RGB and BGR color formats
- Manages button destruction

## Key Types
- CButtonShowColor (Class): Custom button control for color display
- None

## Key Functions
### OnPaint
- Purpose: Renders the color preview in the button control
- Calls: CPaintDC constructor, CPen constructor, CBrush constructor, SelectObject, FillRect, MoveTo, LineTo

### RGBtoBGR
- Purpose: Converts RGB color format to BGR format
- Calls: None

### BGRtoRGB
- Purpose: Converts BGR color format to RGB format
- Calls: RGBtoBGR

## Globals
- None

## Dependencies
- StdAfx.h
- Gameclient/ParticleSys.h
- CButtonShowColor.h
- Windows GDI classes (CPaintDC, CPen, CBrush, CRect)
- MFC message map macros (BEGIN_MESSAGE_MAP, ON_WM_PAINT)
