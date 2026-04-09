# Generals/Code/Tools/WorldBuilder/src/TerrainSwatches.cpp - Enhanced Analysis

## Architectural Role
This file is part of the WorldBuilder tool's UI layer, specifically handling the visual representation of terrain materials. It bridges the terrain data model (via `TerrainMaterial` and `WorldHeightMapEdit`) with the MFC-based UI rendering pipeline.

## Cross-References
### Incoming
- **UI Framework**: MFC message dispatch calls `OnPaint()` during window redraw.
- **Terrain Data**: `TerrainMaterial::getFgTexClass()` and `getBgTexClass()` provide texture class IDs.
- **Heightmap Editor**: `WorldHeightMapEdit::getPointerToClassTileData()` supplies raw texture data.

### Outgoing
- **Rendering**: Uses Windows GDI (`::StretchDIBits`) for texture display.
- **Memory Management**: Allocates/deletes `BITMAPINFO` structs dynamically.

## Design Patterns
- **Observer**: `OnPaint()` reacts to MFC's paint events, typical of MFC's event-driven model.
- **Facade**: Abstracts GDI texture rendering via `DrawMyTexture()`, hiding low-level details from callers.
- **Dependency Injection**: Texture data is injected via `WorldHeightMapEdit` pointers, decoupling rendering from data storage.
