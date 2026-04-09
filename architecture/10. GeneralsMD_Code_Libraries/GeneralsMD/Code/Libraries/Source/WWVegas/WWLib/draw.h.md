# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/draw.h

## Purpose
Header file declaring drawing functions for rendering shapes and blitting blocks on surfaces.

## Responsibilities
- Declares shape drawing and blitting functions
- Defines interfaces for surface manipulation
- Provides remapping and clipping capabilities

## Key Types
None

## Key Functions
### Draw_Shape
- Purpose: Draws a shape from a shape set onto a surface at a specified point.
- Calls: Not inferable

### Blit_Block
- Purpose: Copies a rectangular block from a source surface to a destination surface with optional remapping and clipping.
- Calls: Not inferable

## Globals
None

## Dependencies
- "convert.h" (ConvertClass)
- "point.h" (Point2D)
- "shapeset.h" (ShapeSet, ShapeFlags_Type)
- Surface class
- Rect class
- Blitter class
