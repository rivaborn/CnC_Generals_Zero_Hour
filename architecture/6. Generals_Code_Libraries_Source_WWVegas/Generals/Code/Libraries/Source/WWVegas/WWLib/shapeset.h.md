# Generals/Code/Libraries/Source/WWVegas/WWLib/shapeset.h

## Purpose
Defines the ShapeSet class for managing 2D shape data, including transparency and RLE compression.

## Responsibilities
- Provides access to shape data and metadata
- Handles shape transparency and compression flags
- Validates shape indices
- Manages shape dimensions and offsets

## Key Types
- **ShapeSet (Class)**: Main class for shape data management
- **ShapeRecord (Class)**: Represents individual shape metadata
- **(anonymous enum)**: Shape flags (transparent/RLE)
- **SFLAG_TRANSPARENT (Enum)**: Flag for transparent pixels
- **SFLAG_RLE (Enum)**: Flag for RLE compression

## Key Functions
### ShapeSet::Get_Data
- Purpose: Returns pointer to raw shape data
- Calls: Fetch_Record_Pointer

### ShapeSet::Get_Rect
- Purpose: Returns sub-rectangle for a shape
- Calls: Fetch_Record_Pointer

### ShapeSet::Is_Transparent
- Purpose: Checks if shape contains transparent pixels
- Calls: Fetch_Record_Pointer, ShapeRecord::Is_Transparent

### ShapeSet::Is_RLE_Compressed
- Purpose: Checks if shape is RLE compressed
- Calls: Fetch_Record_Pointer, ShapeRecord::Is_RLE_Compressed

### ShapeSet::Fetch_Record_Pointer
- Purpose: Gets ShapeRecord pointer for a shape index
- Calls: Is_Shape_Index_Valid

## Globals
None

## Dependencies
- "bool.h"
- "trect.h"
- Rect class (used but not defined here)
