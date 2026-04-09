# Generals/Code/Libraries/Source/WWVegas/WWLib/blitblit.h - Enhanced Analysis

## Architectural Role
This file implements low-level pixel manipulation primitives used throughout the SAGE engine's rendering pipeline. It bridges the gap between raw pixel data and higher-level rendering systems by providing optimized blitting operations that handle color space conversion, transparency, and special effects.

## Cross-References
### Incoming
- Rendering systems (e.g., W3D) use these blitters for texture uploads and framebuffer operations
- UI system likely calls these for widget rendering and screen transitions
- Terrain/unit rendering systems use transparency-aware blitters for alpha blending

### Outgoing
- Directly uses `memcpy`/`memmove` from `<string.h>` for basic operations
- Relies on `blitter.h` base class interface
- Assembly implementations interact directly with CPU registers/memory

## Design Patterns
- **Template Method Pattern**: Base `Blitter` class defines interface, subclasses implement specific blit operations
- **Strategy Pattern**: Different blitter classes encapsulate various pixel operations, selectable at runtime
- **Inline Assembly Optimization**: Critical paths implemented in assembly for performance (MSVC-specific)

*Not inferable*: Exact usage patterns in higher-level systems (e.g., when specific blitters are instantiated)
