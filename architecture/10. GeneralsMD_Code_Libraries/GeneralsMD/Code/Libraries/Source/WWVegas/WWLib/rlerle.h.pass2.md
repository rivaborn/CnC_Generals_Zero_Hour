# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/rlerle.h - Enhanced Analysis

## Architectural Role
This file implements RLE (Run-Length Encoded) blitting operations, a critical component of the SAGE engine's rendering pipeline. It provides optimized pixel manipulation routines for transparency, translation, and blending, supporting the engine's need for efficient 2D/3D rendering of game assets.

## Cross-References
### Incoming
- Rendering subsystem (uses RLE blitters for texture/sprite rendering)
- UI system (for menu graphics and HUD elements)
- Animation system (for frame-by-frame RLE data)

### Outgoing
- Calls into `blitter.h` base class
- Uses low-level memory operations (`memcpy` patterns in assembly)
- Relies on pixel format translation tables (likely from graphics subsystem)

## Design Patterns
- **Template Method Pattern**: Base `RLEBlitter` class defines interface, derived classes implement specific blit operations.
- **Strategy Pattern**: Different blitter classes encapsulate various pixel operations (transparency, blending) as interchangeable strategies.
- **Inline Assembly Optimization**: Critical paths use hand-optimized x86 assembly for performance-critical blitting operations.

*Not inferable*: Exact relationship with W3D rendering pipeline or threading model.
