# Generals/Code/Tools/WorldBuilder/include/MyToolbar.h

## Purpose
Defines a custom toolbar class for adjusting cell size in the WorldBuilder tool.

## Responsibilities
- Manages a slider control for cell size adjustment
- Handles slider events and updates
- Provides static callback for cell size changes
- Extends CDialogBar for UI integration

## Key Types
- CellSizeToolBar (Class): Custom toolbar for cell size manipulation

## Key Functions
### OnVScroll
- Purpose: Handles vertical scroll events from the slider control
- Calls: Not inferable

### WindowProc
- Purpose: Overrides window procedure for custom message handling
- Calls: Not inferable

### SetupSlider
- Purpose: Initializes the slider control with appropriate parameters
- Calls: Not inferable

### CellSizeChanged
- Purpose: Static callback invoked when cell size is modified
- Calls: Not inferable

## Globals
- m_staticThis (CellSizeToolBar*): Static instance pointer for the toolbar
- m_cellSlider (CSliderCtrl): Slider control for cell size adjustment

## Dependencies
- CDialogBar (MFC class)
- CSliderCtrl (MFC class)
- afx_msg (MFC macro)
- DECLARE_MESSAGE_MAP() (MFC macro)
- Int (type alias)
