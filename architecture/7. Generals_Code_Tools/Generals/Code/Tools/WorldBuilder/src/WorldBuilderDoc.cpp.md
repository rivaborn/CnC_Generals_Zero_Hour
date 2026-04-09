# Generals/Code/Tools/WorldBuilder/src/WorldBuilderDoc.cpp

## Purpose
Implements the CWorldBuilderDoc class, the core document class for the WorldBuilder map editor tool.

## Responsibilities
- Manages map document serialization (save/load)
- Handles undo/redo functionality
- Provides terrain boundary management
- Implements map data export/dumping
- Manages waypoint links and map objects

## Key Types
- DIRECTION (Enum): Direction preferences for point placement
- MFCFileOutputStream (Class): Output stream wrapper for MFC CFile
- CachedMFCFileOutputStream (Class): Buffered output stream for MFC files
- CompressedCachedMFCFileOutputStream (Class): Compressed buffered output stream

## Key Functions
### FindIndexNearest
- Purpose: Finds the nearest cell index to a point in a preferred direction
- Calls: getCellIndexFromCoord

### IndexInRect
- Purpose: Checks if a cell index is inside a 3D rectangle
- Calls: getCoordFromCellIndex, PointInsideRect3D

### AddUniqueAndNeighbors
- Purpose: Recursively adds cell indices and their neighbors to a list if they're inside a rectangle
- Calls: IndexInRect, AddUniqueAndNeighbors (recursive)

### OnRemoveclifftexmapping
- Purpose: Removes cliff texture mapping from the heightmap with undo support
- Calls: AfxMessageBox, duplicate, removeCliffMapping, updateHeightMap, AddAndDoUndoable

## Globals
- gAlreadyOpen (Bool): Tracks if another WorldBuilder instance is open (only when ONLY_ONE_AT_A_TIME defined)

## Dependencies
- MFC framework classes (CFile, CDocument)
- Game engine classes (WorldHeightMap, MapObject, DataChunkOutput)
- Compression.h for map file compression
- Various game logic headers (ScriptEngine, SidesList, etc.)
