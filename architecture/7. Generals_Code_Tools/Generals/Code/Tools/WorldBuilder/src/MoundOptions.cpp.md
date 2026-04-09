# Generals/Code/Tools/WorldBuilder/src/MoundOptions.cpp

## Purpose
Handles the UI dialog for configuring mound tool parameters in WorldBuilder.

## Responsibilities
- Manages UI controls for brush width, height, and feather settings
- Updates MoundTool with new parameter values
- Handles user input from edit controls and sliders
- Maintains static state for current tool settings

## Key Types
- MoundOptions (Class): Dialog class for mound tool options
- PopSliderButton (Class): Slider control helper (external)

## Key Functions
### setFeather
- Purpose: Updates feather value in UI and static state
- Calls: GetDlgItem, SetWindowText

### setWidth
- Purpose: Updates brush width value in UI and static state
- Calls: GetDlgItem, SetWindowText

### setHeight
- Purpose: Updates mound height value in UI and static state
- Calls: GetDlgItem, SetWindowText

### OnChangeFeatherEdit
- Purpose: Handles feather edit control changes
- Calls: GetWindowText, MoundTool::setFeather, SetWindowText

### OnChangeSizeEdit
- Purpose: Handles brush width edit control changes
- Calls: GetWindowText, MoundTool::setWidth, SetWindowText

### OnChangeHeightEdit
- Purpose: Handles mound height edit control changes
- Calls: GetWindowText, MoundTool::setMoundHeight, SetWindowText

### GetPopSliderInfo
- Purpose: Provides slider control parameters
- Calls: None

### PopSliderChanged
- Purpose: Handles slider value changes
- Calls: GetDlgItem, SetWindowText, MoundTool::setWidth/Height/Feather

## Globals
- m_staticThis (MoundOptions*): Singleton instance pointer
- m_currentWidth (Int): Current brush width value
- m_currentHeight (Int): Current mound height value
- m_currentFeather (Int): Current feather value

## Dependencies
- stdafx.h, resource.h, BaseType.h, MoundOptions.h, WorldBuilderView.h, MoundTool.h
- CDialog, CWnd, CString, COptionsPanel, PopSliderButton
- MoundTool class methods (external)
