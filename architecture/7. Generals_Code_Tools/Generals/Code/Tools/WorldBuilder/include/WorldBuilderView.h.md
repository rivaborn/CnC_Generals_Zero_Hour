# Generals/Code/Tools/WorldBuilder/include/WorldBuilderView.h

## Purpose
Defines the `CWorldBuilderView` class, a MFC view for the WorldBuilder tool, handling 2D map editing visualization.

## Responsibilities
- Render height maps, textures, and objects in 2D view
- Manage scroll offsets and view coordinates
- Handle user input (mouse, scroll) for map navigation
- Maintain grid/contour display settings

## Key Types
- **CWorldBuilderView (Class)**: MFC view for 2D map editing
- **MapObject (Class)**: Reference to map objects (defined elsewhere)
- **CWorldBuilderDoc (Class)**: Reference to document class (defined elsewhere)

## Key Functions
### `drawMyTexture`
- Purpose: Draw a texture bitmap in a rectangle.
- Calls: None visible.

### `getColorForHeight`
- Purpose: Get a color for a height value.
- Calls: None visible.

### `drawContours`
- Purpose: Draw height map contours.
- Calls: `isBetween`, `interpolate`.

### `isBetween`
- Purpose: Check if a value is between two others.
- Calls: None visible.

### `interpolate`
- Purpose: Interpolate a point at a given height.
- Calls: None visible.

### `drawObjectInView`
- Purpose: Draw an object's icon at a given point.
- Calls: None visible.

### `viewToDocCoords`
- Purpose: Convert view coordinates to document coordinates.
- Calls: None visible.

### `docToViewCoords`
- Purpose: Convert document coordinates to view coordinates.
- Calls: None visible.

### `setCenterInView`
- Purpose: Set the center for display.
- Calls: None visible.

### `adjustDocSize`
- Purpose: Adjust view when document size changes.
- C
