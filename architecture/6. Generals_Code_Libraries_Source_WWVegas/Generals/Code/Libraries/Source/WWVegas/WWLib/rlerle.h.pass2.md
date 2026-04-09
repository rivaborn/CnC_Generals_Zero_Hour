# Generals/Code/Libraries/Source/WWVegas/WWLib/rlerle.h - Enhanced Analysis

## Architectural Role
This file implements the core RLE (Run-Length Encoded) decompression logic for the SAGE engine's rendering pipeline. It provides specialized blitter classes that handle various pixel operations (transparency, translation, remapping, darkening, and translucency) during sprite rendering, bridging the gap between compressed asset data and the display system.

## Cross-References
### Incoming
- Rendering subsystem (W3D) - Uses these blitters for sprite rendering
- UI system - Likely uses transparency/translucency blitters for HUD elements
- Particle effects - Uses various blitter types for visual effects

### Outgoing
- `blitter.h` - Inherits from `RLEBlitter` base class
- Assembly optimizations - Directly uses inline assembly for performance-critical paths

## Design Patterns
- **Template Method Pattern** - Uses templated classes to support different pixel formats (e.g., `unsigned short` for 16-bit displays)
- **Strategy Pattern** - Different blitter classes encapsulate various pixel operations (transparency, translucency, etc.)
- **Inline Assembly Optimization** - Critical performance paths use inline assembly for speed (e.g., `RLEBlitTransXlat<unsigned short>::Blit`)

*Not inferable: Exact callers of these blitters (e.g., which rendering functions use which blitter types).*
