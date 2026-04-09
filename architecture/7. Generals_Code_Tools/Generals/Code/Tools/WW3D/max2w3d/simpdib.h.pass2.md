# Generals/Code/Tools/WW3D/max2w3d/simpdib.h - Enhanced Analysis

## Architectural Role
This file defines a lightweight DIB wrapper used in the max2w3d toolchain for asset conversion. It bridges 3DS Max plugin functionality with W3D format requirements, handling palette-based bitmap operations during model/texture export.

## Cross-References
### Incoming
- Likely called by max2w3d tool components (e.g., texture processors, model exporters)
- Potentially referenced by other WW3D tools needing simple DIB manipulation

### Outgoing
- Uses `PaletteClass` for color management (from palette.h)
- Relies on Windows GDI (`HBITMAP`, `BITMAPINFO`) for bitmap creation
- Interfaces with 3DS Max SDK (`Max.h`) for plugin integration

## Design Patterns
- **Wrapper Facade**: Abstracts GDI bitmap complexity behind simple methods
- **Resource Management**: Tracks bitmap handle and memory (Pixels/PixelBase) for proper cleanup
- **Error Handling**: Uses `IsZombie` flag to indicate construction failures (living-dead pattern)
