# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/blitter.h - Enhanced Analysis

## Architectural Role
This header defines core abstraction interfaces for pixel data transfer in the SAGE engine's rendering pipeline. It serves as the foundational contract between the rendering system and various hardware/software blitting implementations.

## Cross-References
### Incoming
- Rendering subsystem (W3D) - uses `Blitter` for texture uploads and framebuffer operations
- UI system - leverages `Blitter` for widget rendering and screen updates
- RLE-compressed asset loading - depends on `RLEBlitter` for decompression

### Outgoing
- None (pure interface header)

## Design Patterns
- **Strategy Pattern**: Abstract blitter interfaces allow runtime selection of optimal blitting implementations (e.g., CPU vs GPU paths)
- **Template Method**: `Blitter::Blit` provides default overlap handling while delegating actual copying to subclasses
- **Interface Segregation**: Separate `RLEBlitter` interface isolates RLE-specific concerns from general blitting

*Not inferable*: Specific concrete implementations or performance optimization strategies.
