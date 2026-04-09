# Generals/Code/Libraries/Source/WWVegas/WWLib/convert.cpp - Enhanced Analysis

## Architectural Role
This file implements the core color conversion and blitting infrastructure for the SAGE engine's rendering pipeline. It bridges the gap between game assets (stored in art palettes) and the display surface (screen palette), handling both 8-bit and 16-bit color formats.

## Cross-References
### Incoming
- Rendering subsystem calls `Blitter_From_Flags` and `RLEBlitter_From_Flags` to get appropriate blitters
- Shape drawing code uses these blitters for actual rendering operations
- Palette management code likely instantiates `ConvertClass`

### Outgoing
- Uses `BlitPlainXlat`, `BlitTransXlat`, and other blitter classes for actual pixel operations
- Depends on `DSurface` for display surface properties (mask values)
- Uses `HSVClass` for color space conversions in shadow table generation

## Design Patterns
- **Factory Method**: `Blitter_From_Flags` and `RLEBlitter_From_Flags` act as factory methods for selecting appropriate blitter implementations
- **Strategy**: Different blitter classes represent different rendering strategies (translucency, remapping, etc.)
- **Composite**: The `ConvertClass` composites multiple blitter objects to handle various rendering scenarios
