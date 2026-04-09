# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/blit.cpp - Enhanced Analysis

## Architectural Role
Core rendering infrastructure providing low-level pixel transfer operations between surfaces and buffers, supporting both uncompressed and RLE-compressed data. Acts as a bridge between the surface abstraction layer and concrete rendering implementations.

## Cross-References
### Incoming
- Rendering pipeline (W3D) - uses blitting for texture/sprite rendering
- UI system - for widget rendering and screen updates
- Animation system - for frame-by-frame sprite updates
- Particle effects - for dynamic visual elements

### Outgoing
- Surface management (`bsurface.h`, `xsurface.h`) - for surface locking/unlocking
- Memory management - via `Buffer` operations
- Blitter implementations - delegates to `Blitter`/`RLEBlitter` subclasses

## Design Patterns
- **Strategy Pattern**: Uses `Blitter`/`RLEBlitter` interfaces to encapsulate different pixel copying algorithms
- **Facade Pattern**: Provides simplified interfaces (`To_Buffer`/`From_Buffer`) hiding surface complexity
- **Template Method**: `Bit_Blit` overloads demonstrate progressive refinement of blitting parameters

*Not inferable*: Exact blitter implementations or surface memory layout details.
