# Generals/Code/Tools/GUIEdit/Source/Dialog Procedures/ColorDialog.cpp

## Purpose
Implements a color picker dialog for the GUIEdit tool, allowing users to select colors in RGB or HSV modes.

## Responsibilities
- Provides color selection via RGB or HSV color models
- Converts between RGB and HSV color spaces
- Handles dialog events for color manipulation
- Displays color previews and gradient bars

## Key Types
- `RGBColorInt` (struct): Integer-based RGB color with alpha
- `RGBColorReal` (struct): Floating-point RGB color with alpha
- `HSVColorReal` (struct): Floating-point HSV color with alpha

## Key Functions
### `rgbToHSV`
- Purpose: Converts RGB color to HSV color space
- Calls: None

### `hsvToRGB`
- Purpose: Converts HSV color to RGB color space
- Calls: None

### `SelectColor`
- Purpose: Displays the color selection dialog and returns the selected color
- Calls: `DialogBox`, `SelectColorDlgProc`

### `SelectColorDlgProc`
- Purpose: Handles dialog messages for the color picker
- Calls: `rgbToHSV`, `hsvToRGB`, `PositionWindowOnScreen`, `InvalidateRect`, `UpdateWindow`, `SetWindowText`, `SetScrollPos`, `SetDlgItemInt`, `GetDlgItemInt`, `SendMessage`, `GetScrollPos`, `EndDialog`

## Globals
- `selectedColor` (RGBColorInt): Stores the currently selected color
- `mode` (Int): Tracks current color mode (RGB or HSV)
- `displayPos` (ICoord2D): Position where the dialog should open

## Dependencies
- Windows API headers (`windows.h`)
- Project-specific headers: `GUIEdit.h`, `Resource.h`, `GUIEditColor.h`, `Properties.h`, `Common/Debug.h`
