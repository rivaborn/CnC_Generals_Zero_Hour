# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/Convert.h - Enhanced Analysis

## Architectural Role
This file defines the core pixel conversion and blitting infrastructure for the SAGE engine's rendering pipeline. It bridges the gap between 8-bit artwork assets and the screen's native pixel format, providing optimized blitters for various visual effects.

## Cross-References
### Incoming
- Rendering subsystems (e.g., `W3D` model rendering, UI drawing)
- Animation systems requiring palette remapping
- Particle effects needing translucency

### Outgoing
- `Blitter` and `RLEBlitter` implementations (concrete blitter classes)
- `PaletteClass` for color conversion logic
- `Surface` for destination buffer access

## Design Patterns
- **Strategy Pattern**: Different blitter objects encapsulate various rendering strategies (transparency, translucency), selected at runtime via `Blitter_From_Flags`.
- **Flyweight Pattern**: Translation tables (`Translator`, `ShadowTable`) are shared across multiple blit operations to reduce memory usage.
- **Facade Pattern**: `ConvertClass` abstracts complex pixel conversion and blitting into a unified interface.
