# Generals/Code/Tools/WorldBuilder/include/TerrainSwatches.h - Enhanced Analysis

## Architectural Role
This header defines a UI component for the WorldBuilder tool, specifically for previewing terrain textures. It bridges the MFC-based UI layer with the game's terrain rendering system, allowing level designers to visualize terrain materials.

## Cross-References
### Incoming
- Likely called by WorldBuilder's main window or terrain editing dialogs to display texture swatches.

### Outgoing
- Uses MFC (`CWnd`, `CDC`) for Windows UI rendering.
- Depends on `BaseType.h` for basic types, suggesting integration with the engine's type system.

## Design Patterns
- **Observer Pattern**: The class inherits from `CWnd` and uses `DECLARE_MESSAGE_MAP`, indicating it reacts to Windows messages (events).
- **Facade Pattern**: Abstracts terrain texture rendering for the UI layer, hiding underlying W3D texture handling.
