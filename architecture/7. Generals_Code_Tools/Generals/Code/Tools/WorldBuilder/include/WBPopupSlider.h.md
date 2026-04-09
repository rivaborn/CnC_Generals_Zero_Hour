# Generals/Code/Tools/WorldBuilder/include/WBPopupSlider.h

## Purpose
Defines classes for a popup slider UI control used in WorldBuilder.

## Responsibilities
- Declares `PopupSliderOwner` interface for slider callbacks
- Defines `WBPopupSliderButton` (slider button control)
- Implements `PopupSlider` (popup slider window)
- Manages slider state and user interaction

## Key Types
- **PopupSliderOwner (Class)**: Interface for slider event callbacks
- **WBPopupSliderButton (Class)**: Button control that triggers the slider
- **PopupSlider (Class)**: Popup slider window with thumb and channel
- **None**: No enums/structs

## Key Functions
### PopupSlider::New
- Purpose: Factory method to create and show the popup slider
- Calls: `Create`

### PopupSlider::OnLButtonDown
- Purpose: Handles mouse down on slider thumb
- Calls: `MoveThumbUnderMouse`

### PopupSlider::OnMouseMove
- Purpose: Updates slider value during thumb drag
- Calls: `MoveThumbUnderMouse`, `mSliderOwner->PopSliderChanged`

### PopupSlider::OnKeyDown
- Purpose: Handles keyboard input for slider navigation
- Calls: `mSliderOwner->PopSliderChanged`

## Globals
- **PopupSlider::gPopupSlider (PopupSlider*)**: Singleton instance of the popup slider

## Dependencies
- MFC classes (`CButton`, `CWnd`, `CBrush`)
- Windows types (`HICON`, `RECT`, `CPoint`)
- `Bool`/`Int` types (custom or MFC)
- `DECLARE_MESSAGE_MAP()` macro
