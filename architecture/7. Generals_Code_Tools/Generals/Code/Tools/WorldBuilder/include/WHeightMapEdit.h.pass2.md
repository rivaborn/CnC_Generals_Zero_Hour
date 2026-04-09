# Generals/Code/Tools/WorldBuilder/include/WHeightMapEdit.h - Enhanced Analysis

## Architectural Role
This header defines the core terrain editing class for WorldBuilder, extending the runtime `WorldHeightMap` with tool-specific functionality. It bridges the gap between the game's terrain representation and the editor's needs, handling texture management, heightmap modifications, and map object manipulation.

## Cross-References
### Incoming
- **WorldBuilder UI**: Calls editing methods like `blendTile`, `setHeight`, and `floodFill`
- **Map Save/Load**: Uses `saveToFile` and constructor for serialization
- **Texture System**: Relies on `TerrainType` and external texture loading

### Outgoing
- **W3D Rendering**: Inherits from `WorldHeightMap`, calls into W3D device for texture operations
- **Chunk I/O**: Uses `DataChunkOutput` for file operations
- **Game Logic**: Interacts with `MapObject` for object placement

## Design Patterns
- **Template Method**: `loadBaseImages` delegates to `loadDirectoryOfImages` and `loadImagesFromTerrainType`
- **Composite**: Texture classes contain multiple tiles (`TGlobalTextureClass`)
- **Observer**: Warning flags (`m_warnTooManyTex`) suggest event-driven texture management

*(Token count: 198)*
