# Generals/Code/Libraries/Source/WWVegas/WWLib/draw.h - Enhanced Analysis

## Architectural Role
This header defines low-level 2D rendering primitives used by the SAGE engine's rendering pipeline. It bridges the WWLib's surface manipulation capabilities with the higher-level W3D rendering system, providing essential blitting and shape drawing functionality.

## Cross-References
### Incoming
- `Generals/Code/Libraries/Source/WWVegas/WW3D2/textdraw.h` (uses `Blit_Block` for text rendering)

### Outgoing
- Depends on `Surface`, `ConvertClass`, `ShapeSet`, `Rect`, and `Blitter` classes from WWLib
- Likely called by UI rendering systems and 2D overlay components

## Design Patterns
- **Facade Pattern**: Exposes simplified drawing operations while hiding underlying surface manipulation complexity
- **Strategy Pattern**: `Blitter` parameter allows runtime selection of blitting algorithms (e.g., for different hardware acceleration paths)
- **Dependency Injection**: `ConvertClass` and `remap` parameters injected to customize rendering behavior
