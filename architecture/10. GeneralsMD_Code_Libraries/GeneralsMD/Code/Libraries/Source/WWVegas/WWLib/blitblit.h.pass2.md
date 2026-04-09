# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/blitblit.h - Enhanced Analysis

## Architectural Role
This file implements low-level pixel manipulation primitives used throughout the SAGE engine's rendering pipeline. It bridges the gap between raw pixel data operations and higher-level rendering systems by providing optimized blitting operations that handle format conversions and transparency.

## Cross-References
### Incoming
- Rendering subsystems (likely in W3D module) that need to copy/transform pixel data
- UI systems that require bitmap manipulation
- Terrain/unit rendering that uses transparency and remapping
- Video playback systems that need format conversion

### Outgoing
- Directly uses C standard library functions (memcpy/memmove)
- Relies on assembly optimizations for performance-critical paths
- Depends on the base Blitter class interface defined in blitter.h

## Design Patterns
- **Template Method Pattern**: Used for pixel format independence (8-bit vs 16-bit)
- **Strategy Pattern**: Different blitter classes implement various pixel operations
- **Inline Assembly**: For performance-critical pixel operations where C can't match hand-optimized assembly

The assembly implementations reveal this was a performance-sensitive component where the team prioritized cycle-accurate optimizations for common operations like transparency checking and format conversion.
