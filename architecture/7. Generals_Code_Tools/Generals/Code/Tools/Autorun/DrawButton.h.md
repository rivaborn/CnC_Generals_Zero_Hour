# Generals/Code/Tools/Autorun/DrawButton.h

## Purpose
Defines a `DrawButton` class for rendering and managing UI buttons with different states (normal, pressed, focus).

## Responsibilities
- Manage button state and appearance
- Handle bitmap and text rendering
- Provide accessors for button properties
- Check mouse hover state

## Key Types
- **DrawButton (Class)**: Represents a UI button with state management and rendering.
- **BUTTON_STATE (Enum)**: Button states (normal, pressed, focus).
- **NORMAL_STATE (Enum)**: Normal button state.
- **PRESSED_STATE (Enum)**: Pressed button state.
- **FOCUS_STATE (Enum)**: Focused button state.

## Key Functions
### DrawButton (Constructors)
- Purpose: Initialize button with ID, position, bitmaps, text, and font.
- Calls: None.

### Return_Bitmap
- Purpose: Return the current bitmap based on button state.
- Calls: None.

### Draw_Text
- Purpose: Render button text using the provided font.
- Calls: None.

### Is_Mouse_In_Region
- Purpose: Check if mouse coordinates are within the button area.
- Calls: None.

### Set_Stretched_Width / Set_Stretched_Height
- Purpose: Set custom stretched dimensions for the button.
- Calls: None.

## Globals
- None.

## Dependencies
- `<tchar.h>`, `<stdlib.h>`, `"ttfont.h"`
- `RECT`, `Rect`, `TTFontClass`, `MAX_PATH`, `_MAX_FNAME` (external types).
