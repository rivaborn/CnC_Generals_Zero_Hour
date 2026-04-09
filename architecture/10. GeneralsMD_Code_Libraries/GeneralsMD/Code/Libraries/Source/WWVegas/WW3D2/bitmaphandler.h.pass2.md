# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/bitmaphandler.h - Enhanced Analysis

## Architectural Role
This file is a core utility in the SAGE engine's rendering pipeline, handling low-level pixel format conversions and color space operations. It bridges the gap between raw texture data and the engine's internal representation, supporting both Direct3D-compatible formats and legacy paletted textures.

## Cross-References
### Incoming
- **Rendering subsystem**: Uses `BitmapHandlerClass` for texture loading and manipulation (e.g., `WW3D2` texture management).
- **Material system**: Likely called during material initialization for format conversion.
- **Particle effects**: Uses `Copy_Pixel` with HSV shifts for dynamic color effects.

### Outgoing
- **Color space utilities**: Calls `Recolor` (from `colorspace.h`) for HSV adjustments.
- **Assertion system**: Uses `Bitmap_Assert` for format validation.
- **Memory management**: Relies on external `Get_Bytes_Per_Pixel` for pitch calculations.

## Design Patterns
- **Static Utility Class**: `BitmapHandlerClass` is purely static, avoiding instance overhead for frequently used operations.
- **Format-Specific Dispatch**: Uses `switch` on `WW3DFormat` to handle each pixel format, enabling compile-time optimization for common cases.
- **Data-Oriented Design**: Functions operate on raw pointers and pitches, minimizing abstraction overhead for performance-critical paths.
