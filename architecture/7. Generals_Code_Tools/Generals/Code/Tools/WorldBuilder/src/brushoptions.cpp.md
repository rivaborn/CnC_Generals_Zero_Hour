# Generals/Code/Tools/WorldBuilder/src/brushoptions.cpp

## Purpose
Handles the UI dialog for brush tool options in WorldBuilder, managing width, height, and feather settings.

## Responsibilities
- Manages brush tool parameter UI (width, height, feather)
- Updates BrushTool with new parameter values
- Handles slider and edit control interactions
- Maintains static state for current brush settings

## Key Types
- BrushOptions (Class): Main dialog class for brush options
- None: No other significant types defined

## Key Functions
### setFeather
- Purpose: Updates feather value in UI and static state
- Calls: None

### setWidth
- Purpose: Updates brush width in UI and static state
- Calls: None

### setHeight
- Purpose: Updates brush height in UI and static state
- Calls: None

### OnChangeFeatherEdit
- Purpose: Handles feather edit control changes
- Calls: BrushTool::setFeather

### OnChangeSizeEdit
- Purpose: Handles width edit control changes
- Calls: BrushTool::setWidth

### OnChangeHeightEdit
- Purpose: Handles height edit control changes
- Calls: BrushTool::setHeight

### GetPopSliderInfo
- Purpose: Provides slider configuration for popup controls
- Calls: None

### PopSliderChanged
- Purpose: Handles slider value changes
- Calls: BrushTool::setWidth, BrushTool::setHeight, BrushTool::setFeather

## Globals
- m_staticThis (BrushOptions*): Singleton instance pointer
- m_currentWidth (Int): Current brush width value
- m_currentHeight (Int): Current brush height value
- m_currentFeather (Int): Current feather value

## Dependencies
- stdafx.h, resource.h, BaseType.h, brushoptions.h, WorldBuilderView.h, BrushTool.h
- CDialog, CWnd, CString, COptionsPanel, DEBUG_CRASH
- BrushTool class methods (external)
