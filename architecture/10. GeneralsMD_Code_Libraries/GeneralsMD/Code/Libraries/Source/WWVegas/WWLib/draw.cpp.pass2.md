# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/draw.cpp - Enhanced Analysis

## Architectural Role
This file is a core rendering component in the SAGE engine's 2D rendering pipeline, bridging between high-level game objects and low-level blitting operations. It handles the actual drawing of game assets (shapes) onto surfaces while managing compression formats (RLE) and ownership remapping.

## Cross-References
### Incoming
- **Rendering System**: `TextDrawClass` (WW3D2) likely calls `Draw_Shape` for UI elements
- **Game Logic**: Unit/building rendering systems use `Draw_Shape` for in-game assets
- **UI System**: Menu and HUD rendering components call `Blit_Block` for static elements

### Outgoing
- **Blitting Subsystem**: Directly uses `Bit_Blit` and `RLE_Blit` from `blitblit.h`
- **Surface Management**: Interacts with `Surface` and `BSurface` classes for pixel operations
- **Shape System**: Relies on `ShapeSet` for shape data access and `ConvertClass` for pixel conversion

## Design Patterns
- **Strategy Pattern**: Uses `Blitter` and `RLEBlitter` as interchangeable algorithms selected at runtime via `Blitter_From_Flags`
- **Facade Pattern**: Provides high-level `Draw_Shape`/`Blit_Block` interfaces that hide complex blitting operations
- **Composite Pattern**: `ShapeSet` aggregates multiple shapes while `Draw_Shape` treats them uniformly

**Key Insight**: The file demonstrates tight coupling between rendering and compression systems - RLE handling is deeply integrated into the drawing pipeline rather than being a separate layer. This suggests performance optimization was prioritized over modularity in the rendering path.
