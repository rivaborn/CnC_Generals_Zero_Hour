# Generals/Code/Libraries/Source/WWVegas/WW3D2/bitmaphandler.h - Enhanced Analysis

## Architectural Role
This file is a core utility in the SAGE engine's rendering pipeline, handling low-level pixel format conversions and texture operations. It bridges the gap between raw texture data and the engine's internal representation (BGRA/D3D format), supporting both CPU-side operations and GPU texture uploads.

## Cross-References
### Incoming
- **Rendering subsystem**: Uses `BitmapHandlerClass` for texture loading/processing (e.g., `TextureClass`, `MaterialClass`)
- **Resource loading**: Called during asset initialization (e.g., `W3DLoader`)
- **Mipmapping**: Invoked by texture management for LOD generation

### Outgoing
- **WW3DFormat**: Relies on `ww3dformat.h` for format definitions
- **Assert system**: Uses `Bitmap_Assert` for error checking
- **Math utilities**: Implicitly depends on bitwise operations for color math

## Design Patterns
- **Static Utility Class**: All methods are static, providing pure functionality without state.
- **Format Adapter**: Abstracts pixel format conversions, decoupling source/destination formats.
- **Inline Optimization**: Uses `WWINLINE` for performance-critical pixel operations.

*Not inferable*: No clear use of Factory, Observer, or other patterns.
