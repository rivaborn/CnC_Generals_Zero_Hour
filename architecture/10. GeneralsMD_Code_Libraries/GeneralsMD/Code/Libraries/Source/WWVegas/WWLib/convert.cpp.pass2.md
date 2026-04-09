# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/convert.cpp - Enhanced Analysis

## Architectural Role
This file implements the core rendering pipeline's color conversion and blitting infrastructure, bridging art assets (8-bit palette) with display surfaces (8-bit or 16-bit). It's a critical abstraction layer enabling cross-format rendering in the SAGE engine.

## Cross-References
### Incoming
- Rendering subsystems (e.g., shape drawing, UI elements) call `Blitter_From_Flags`/`RLEBlitter_From_Flags` to obtain appropriate blitters for drawing operations.
- Likely invoked during game initialization (e.g., when setting up display surfaces) via `ConvertClass` constructor.

### Outgoing
- Depends on `DSurface` for display-specific pixel manipulation (mask values, remap tables).
- Uses `HSVClass` for color space conversions (shadow table generation).
- Instantiates various `Blit*` and `RLEBlit*` classes (external blitter implementations).

## Design Patterns
- **Factory Method**: `Blitter_From_Flags`/`RLEBlitter_From_Flags` act as factory methods for selecting blitters based on runtime flags.
- **Strategy**: Blitter objects encapsulate different rendering strategies (transparency, translucency), allowing dynamic selection.
- **Object Pooling**: Blitter instances are created once during `ConvertClass` initialization and reused (not inferable if pooled, but likely given performance constraints).
