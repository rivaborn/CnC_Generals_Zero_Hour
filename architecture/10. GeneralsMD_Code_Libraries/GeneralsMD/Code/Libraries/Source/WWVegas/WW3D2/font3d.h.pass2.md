# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/font3d.h - Enhanced Analysis

## Architectural Role
This file defines the core 3D font rendering system in the SAGE engine, bridging the rendering pipeline (WW3D2) with the UI system. It handles font texture management, character metrics, and scaling, serving as the foundation for all in-game text rendering.

## Cross-References
### Incoming
- UI rendering systems (e.g., HUD, menus)
- Localization systems (WCHAR support)
- Rendering pipeline (texture/surface management)

### Outgoing
- TextureClass/SurfaceClass for font asset loading
- Vector4/RectClass for UV coordinate calculations
- RefCountClass for memory management

## Design Patterns
- **Resource Management**: Uses RefCountClass for font data sharing
- **Flyweight**: Font3DDataClass as shared data, Font3DInstanceClass as context-specific instances
- **Lazy Initialization**: Scaled metrics built only when needed (Build_Cached_Tables)
