# Generals/Code/Libraries/Source/WWVegas/WWLib/blit.cpp - Enhanced Analysis

## Architectural Role
This file implements core pixel transfer operations for the SAGE engine's rendering pipeline, bridging between surface management (BSurface/XSurface) and the actual blitting logic. It handles both raw and RLE-compressed data transfers with clipping, serving as the low-level workhorse for sprite rendering and texture operations.

## Cross-References
### Incoming
- Rendering subsystems (e.g., sprite drawing, UI elements)
- Animation systems (for frame-by-frame blitting)
- Particle effects (for buffer-based operations)
- Modding infrastructure (custom blit operations)

### Outgoing
- `BSurface`/`XSurface` for surface locking/unlocking
- `Blitter`/`RLEBlitter` for actual pixel operations
- `Blit_Clip` for rectangle clipping logic

## Design Patterns
- **Strategy Pattern**: Uses `Blitter`/`RLEBlitter` abstractions to encapsulate different pixel transfer algorithms
- **Facade Pattern**: Provides high-level blit functions that delegate to lower-level surface operations
- **Adapter Pattern**: Converts between surface and buffer representations via `To_Buffer`/`From_Buffer`
