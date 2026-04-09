# Generals/Code/Tools/WorldBuilder/src/SelectMacrotexture.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI dialog for selecting macrotextures in WorldBuilder, bridging the gap between the file system, terrain rendering, and global state management. It serves as a tool-specific UI layer that interacts with core engine systems.

## Cross-References
### Incoming
- Not inferable (no explicit callers visible in this file)

### Outgoing
- **FileSystem**: Uses `TheFileSystem->getFileListInDirectory` to scan for TGA files
- **Terrain Rendering**: Calls `TheTerrainRenderObject->updateMacroTexture` to apply selected textures
- **Global Data**: Modifies `TheWritableGlobalData->m_useLightMap` to enable lighting

## Design Patterns
- **Observer Pattern**: The `OnNotify` handler reacts to tree view selection changes, updating terrain state
- **MVC (Model-View-Controller)**: Separates texture selection UI (view) from terrain rendering logic (model/controller)
- **Singleton Access**: Uses global instances (`TheFileSystem`, `TheTerrainRenderObject`) for subsystem access

*Not inferable: Factory, Strategy, or Template patterns not evident in this file.*
