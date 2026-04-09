# Generals/Code/Libraries/Source/WWVegas/WWLib/Convert.h - Enhanced Analysis

## Architectural Role
This file defines the core pixel conversion and blitting infrastructure for the SAGE engine's 2D rendering pipeline. It bridges the gap between 8-bit artwork assets and the target display's pixel format while providing specialized blitters for various visual effects.

## Cross-References
### Incoming
- Rendering subsystems (e.g., `ShapeClass`, `RLEShapeClass`) use `ConvertClass` for pixel conversion and blitting
- UI components likely depend on `Blitter_From_Flags` for UI element rendering
- Animation systems may use `RLEBlitter_From_Flags` for compressed animations

### Outgoing
- Directly uses `Blitter` and `RLEBlitter` classes for actual pixel operations
- Relies on `PaletteClass` for color translation tables
- Interfaces with `Surface` for destination buffer access

## Design Patterns
- **Strategy Pattern**: Different blitter objects (e.g., `TransBlitter`, `ShadowBlitter`) are selected at runtime based on flags
- **Flyweight Pattern**: Translation tables are reused across multiple conversion operations
- **Facade Pattern**: Hides complex pixel conversion details behind simple methods like `Convert_Pixel`
