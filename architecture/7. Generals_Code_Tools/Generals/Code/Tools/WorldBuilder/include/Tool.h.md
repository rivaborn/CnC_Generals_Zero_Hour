# Generals/Code/Tools/WorldBuilder/include/Tool.h

## Purpose
Defines the base `Tool` class for the WorldBuilder editor, providing an interface for terrain editing tools.

## Responsibilities
- Declares the abstract `Tool` class and its core methods
- Defines helper enums and types for terrain manipulation
- Provides static utility functions for brush calculations
- Manages cursor and tool activation state

## Key Types
- `TTrackingMode` (Enum): mouse tracking modes (none, left, middle, right)
- `VecHeightMapIndexes` (Type): vector of `CPoint` for storing heightmap indices
- `Tool` (Class): base class for WorldBuilder editing tools

## Key Functions
### `Tool(Int toolID, Int cursorID)`
- Purpose: Constructs a tool with given UI IDs.
- Calls: None

### `setCursor()`
- Purpose: Sets the tool's cursor.
- Calls: None

### `activate()`
- Purpose: Activates the tool as the current tool.
- Calls: None

### `mouseMoved(TTrackingMode m, CPoint viewPt, WbView* pView, CWorldBuilderDoc *pDoc)`
- Purpose: Handles mouse movement events.
- Calls: None

### `mouseDown(TTrackingMode m, CPoint viewPt, WbView* pView, CWorldBuilderDoc *pDoc)`
- Purpose: Handles mouse down events.
- Calls: None

### `mouseUp(TTrackingMode m, CPoint viewPt, WbView* pView, CWorldBuilderDoc *pDoc)`
- Purpose: Handles mouse up events.
- Calls: None

### `calcRoundBlendFactor(CPoint center, Int x, Int y, Int brushWidth, Int featherWidth)`
- Purpose: Calculates blend factor for round brushes.
- Calls: None
