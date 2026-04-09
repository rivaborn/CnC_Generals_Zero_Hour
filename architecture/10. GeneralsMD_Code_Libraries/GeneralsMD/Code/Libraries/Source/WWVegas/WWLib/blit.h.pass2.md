# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/blit.h - Enhanced Analysis

## Architectural Role
This header defines the core blitting operations for the SAGE engine's rendering pipeline, serving as the low-level interface for surface-to-surface transfers and buffer conversions. It bridges the abstract Surface/SurfaceRect classes with concrete blitting implementations (Bit_Blit, RLE_Blit) and buffer serialization.

## Cross-References
### Incoming
- `GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/blitblit.h` (BlitForward/BlitBackward)
- Rendering subsystems (e.g., W3D model rendering, UI drawing)
- Surface management (Surface/SurfaceRect classes)

### Outgoing
- `blitter.h` (Blitter/RLEBlitter classes)
- `buff.h` (Buffer class)
- `surface.h` (Surface/SurfaceRect classes)

## Design Patterns
- **Strategy Pattern**: Blitter/RLEBlitter classes are passed as parameters, allowing runtime selection of blitting algorithms.
- **Facade Pattern**: Encapsulates complex surface operations behind simple function calls (e.g., clipping, RLE decompression).
- **Not inferable**: No clear use of other patterns (e.g., no factories, observers, or decorators visible in the header).
