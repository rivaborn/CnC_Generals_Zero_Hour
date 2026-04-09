# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/shapeset.h

## Purpose
Defines the ShapeSet class for managing 2D shape data, including transparency and RLE compression.

## Responsibilities
- Provide access to shape data and metadata
- Handle shape indexing and validation
- Expose shape properties (rect, transparency, compression)
- Manage shape records and their flags

## Key Types
- **ShapeSet (Class)**: Main container for shape data and records.
- **ShapeRecord (Class)**: Represents individual shape metadata (offset, size, flags).
- **(anonymous enum)**: Shape flags (transparent, RLE-compressed).
- **SFLAG_TRANSPARENT (Enum)**: Flag for transparent pixels.
- **SFLAG_RLE (Enum)**: Flag for RLE compression.

## Key Functions
### ShapeSet::Get_Data
- Purpose: Returns pointer to raw shape data.
- Calls: Fetch_Record_Pointer

### ShapeSet::Get_Rect
- Purpose: Returns the sub-rectangle of a shape.
- Calls: Fetch_Record_Pointer

### ShapeSet::Is_Transparent
- Purpose: Checks if a shape has transparent pixels.
- Calls: Fetch_Record_Pointer, ShapeRecord::Is_Transparent

### ShapeSet::Is_RLE_Compressed
- Purpose: Checks if a shape is RLE-compressed.
- Calls: Fetch_Record_Pointer, ShapeRecord::Is_RLE_Compressed

### ShapeSet::Fetch_Record_Pointer
- Purpose: Retrieves ShapeRecord pointer for a given shape index.
- Calls: Is_Shape_Index_Valid

## Globals
None

## Dependencies
- "bool.h", "trect.h"
- Rect (used for shape rectangles)
