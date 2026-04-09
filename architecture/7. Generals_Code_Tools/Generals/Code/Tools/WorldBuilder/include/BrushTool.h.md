# Generals/Code/Tools/WorldBuilder/include/BrushTool.h

## Purpose
Defines the BrushTool class for terrain height editing in WorldBuilder.

## Responsibilities
- Manages height brush tool operations
- Handles mouse input for terrain modification
- Maintains brush parameters (width, feather, height)
- Provides access to height map edits

## Key Types
- BrushTool (Class): Terrain height editing tool
- WorldHeightMapEdit (Class): Reference to height map edits (external)

## Key Functions
### BrushTool()
- Purpose: Constructor for BrushTool
- Calls: None

### ~BrushTool()
- Purpose: Destructor for BrushTool
- Calls: None

### setWidth(Int width)
- Purpose: Sets the brush width
- Calls: None

### setFeather(Int feather)
- Purpose: Sets the brush feather
- Calls: None

### setHeight(Int height)
- Purpose: Sets the brush height
- Calls: None

### mouseDown(TTrackingMode m, CPoint viewPt, WbView* pView, CWorldBuilderDoc *pDoc)
- Purpose: Handles mouse down event for brush tool
- Calls: None

### mouseUp(TTrackingMode m, CPoint viewPt, WbView* pView, CWorldBuilderDoc *pDoc)
- Purpose: Handles mouse up event for brush tool
- Calls: None

### mouseMoved(TTrackingMode m, CPoint viewPt, WbView* pView, CWorldBuilderDoc *pDoc)
- Purpose: Handles mouse movement for brush tool
- Calls: None

### activate()
- Purpose: Activates the brush tool
- Calls: None

## Globals
- m_brushWidth (Int): Current brush width
- m_brushFeather (Int): Current brush feather
- m_brushSquare (Bool):
