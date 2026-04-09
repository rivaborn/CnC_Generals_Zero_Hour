# Generals/Code/Tools/WorldBuilder/src/MyToolbar.cpp

## Purpose
Handles the cell size slider toolbar in WorldBuilder, allowing users to adjust grid cell size.

## Responsibilities
- Manages a vertical slider for cell size selection
- Updates the view when slider position changes
- Maintains a static instance for global access
- Converts slider positions to actual cell sizes (powers of 2)

## Key Types
- CellSizeToolBar (Class): Main toolbar class handling slider behavior
- None: No additional structs/enums defined

## Key Functions
### CellSizeChanged
- Purpose: Updates slider position based on current cell size
- Calls: m_cellSlider.SetPos

### SetupSlider
- Purpose: Initializes the slider control with proper range and position
- Calls: m_cellSlider.Create, m_cellSlider.SetRange, m_cellSlider.SetPos

### OnVScroll
- Purpose: Handles slider scroll events and updates cell size
- Calls: m_cellSlider.GetPos, pView->setCellSize

### WindowProc
- Purpose: Custom window message handler for scroll events
- Calls: OnVScroll

## Globals
- m_staticThis (CellSizeToolBar*): Static pointer to the toolbar instance

## Dependencies
- CDialogBar, CScrollBar, CRect (MFC)
- CWorldBuilderView, CWorldBuilderDoc (WorldBuilder classes)
- ID_SLIDER, ID_SLIDER (resource IDs)
