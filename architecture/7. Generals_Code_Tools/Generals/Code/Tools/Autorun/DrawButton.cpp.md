# Generals/Code/Tools/Autorun/DrawButton.cpp

## Purpose
Implements a custom button class for the Autorun tool, handling drawing, state management, and mouse interaction.

## Responsibilities
- Manages button state (normal, focus, pressed)
- Handles bitmap-based button rendering
- Processes mouse hover/click detection
- Provides text rendering with different states
- Exposes button dimensions and bitmap paths

## Key Types
- **DrawButton (Class)**: Custom button control with bitmap and text rendering
- **Rect (Struct)**: Rectangle helper for positioning
- **ButtonState (Enum)**: NORMAL_STATE, FOCUS_STATE, PRESSED_STATE

## Key Functions
### DrawButton::DrawButton
- Purpose: Constructs a button with position, dimensions, and bitmap paths
- Calls: wcscpy, memset, Msg

### DrawButton::Is_Mouse_In_Region
- Purpose: Checks if mouse coordinates are within button bounds
- Calls: None

### DrawButton::Return_Bitmap
- Purpose: Returns the bitmap path based on current button state
- Calls: None

### DrawButton::Return_Area
- Purpose: Returns button dimensions in a RECT or Rect struct
- Calls: None

### DrawButton::Set_Stretched_Width/Set_Stretched_Height
- Purpose: Adjusts button drawing dimensions while preserving original size
- Calls: None

## Globals
- **TheGameText (GameText)**: Used for localized string fetching (non-LEAN_AND_MEAN only)

## Dependencies
- Windows.h, windowsx.h
- autorun.h, drawbutton.h, locale_api.h, wnd_file.h
- Common/UnicodeString.h, Common/SubsystemInterface.h, GameClient/GameText.h (non-LEAN_AND_MEAN)
