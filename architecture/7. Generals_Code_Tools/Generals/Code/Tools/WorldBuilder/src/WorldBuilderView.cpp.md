# Generals/Code/Tools/WorldBuilder/src/WorldBuilderView.cpp

## Purpose
Handles the 2D rendering and interaction of the map editor's view, including terrain, grid, contours, and object icons.

## Responsibilities
- Renders height maps, textures, grid, and contours
- Manages view scrolling and zooming
- Handles coordinate conversion between screen and document space
- Processes user input for map editing
- Maintains display preferences (grid, contours, textures)

## Key Types
- **CWorldBuilderView (Class)**: Main view class for the map editor
- **WorldHeightMapEdit (Class)**: Height map data structure
- **Coord3D (Struct)**: 3D coordinate representation

## Key Functions
### OnPaint
- Purpose: Renders the map view with terrain, grid, contours, and objects
- Calls: getColorForHeight, drawContours, drawMyTexture, docToViewCoords

### getColorForHeight
- Purpose: Generates color based on height value for terrain visualization
- Calls: None

### scrollInView
- Purpose: Handles view scrolling in response to user input
- Calls: ScrollWindow, SetScrollPos

### viewToDocCoords / docToViewCoords
- Purpose: Converts between screen coordinates and document coordinates
- Calls: None

## Globals
- **m_cellSize (Int)**: Current zoom level (pixel size per cell)
- **m_showContours (Bool)**: Flag for contour line display
- **mXScrollOffset/mYScrollOffset (Int)**: Current scroll position
- **mShowGrid (Bool)**: Flag for grid display
- **m_showTexture (Bool)**: Flag for texture display

## Dependencies
- **WbView**: Base view class
- **WorldBuilderDoc**: Document class containing map data
- **WorldHeightMapEdit**: Height map editing class
- **ContourOptions**: Contour rendering settings
- **CUndoable**: Undo/redo system
- **MFC classes**: CDC, CScrollBar, CBrush, etc.
- **W3DDevice components**: HeightMap, W3DRoadBuffer
