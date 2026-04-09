# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/draw.h - Enhanced Analysis

## Architectural Role
This header defines low-level 2D rendering primitives used by the SAGE engine's rendering pipeline. It bridges the WWLib's surface manipulation capabilities with the W3D renderer's shape-based drawing system.

## Cross-References
### Incoming
- `GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/textdraw.h` (uses `Blit_Block` for text rendering)

### Outgoing
- Relies on `Surface`, `ConvertClass`, `ShapeSet`, and `Blitter` abstractions from WWLib
- Implicitly depends on W3D's shape system for `Draw_Shape`

## Design Patterns
- **Facade Pattern**: Exposes simplified drawing operations while hiding underlying surface/blitter complexity
- **Strategy Pattern**: `Blitter` parameter allows runtime selection of blitting algorithms (e.g., for different hardware acceleration paths)
- **Dependency Injection**: `ConvertClass` and `remap` parameters injected for runtime flexibility in color conversion/remapping

*Not inferable*: No clear use of Observer or Factory patterns in this header alone.
