# Generals/Code/Tools/WorldBuilder/src/WBPopupSlider.cpp

## Purpose
Implements a popup slider control for the WorldBuilder tool, allowing users to adjust values via a draggable thumb.

## Responsibilities
- Manages `WBPopupSliderButton` for triggering sliders
- Handles `PopupSlider` creation, rendering, and interaction
- Processes mouse/keyboard input for slider manipulation
- Notifies owner of value changes via callback interface

## Key Types
- `WBPopupSliderButton` (Class): Button that spawns a popup slider
- `PopupSlider` (Class): The draggable slider window
- `PopupSliderOwner` (Interface): Abstract owner for slider callbacks

## Key Functions
### `PopupSlider::New`
- Purpose: Creates and positions a new popup slider
- Calls: `GetPopSliderInfo`, `Create`, `GetThumbIconRect`, `SetWindowPos`

### `PopupSlider::OnLButtonDown`
- Purpose: Handles mouse down events for thumb dragging or channel clicks
- Calls: `GetThumbIconRect`, `GetChannelRect`, `MoveThumbUnderMouse`

### `PopupSlider::OnMouseMove`
- Purpose: Updates slider value during thumb drag
- Calls: `MoveThumbUnderMouse`, `PopSliderChanged`

### `PopupSlider::MoveThumbUnderMouse`
- Purpose: Calculates new slider value based on mouse position
- Calls: `GetChannelRect`, `GetThumbIconRect`, `InvalidateRect`

## Globals
- `gPopupSlider` (PopupSlider*): Tracks the active slider instance

## Dependencies
- MFC (`CWnd`, `CButton`, `CPaintDC`)
- Windows API (`LoadImage`, `DrawIconEx`)
- `PopupSliderOwner` interface (external)
- Resource IDs (`IDB_DownArrow`, `IDI_Thumb`)
