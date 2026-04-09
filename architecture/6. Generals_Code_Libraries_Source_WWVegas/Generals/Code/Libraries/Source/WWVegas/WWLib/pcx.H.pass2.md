# Generals/Code/Libraries/Source/WWVegas/WWLib/pcx.H - Enhanced Analysis

## Architectural Role
This header defines the PCX image format I/O interface, bridging the low-level file system (FileClass) with the rendering pipeline (Surface/PaletteClass). It serves as a legacy image loader for the SAGE engine, likely used for loading pre-rendered assets or UI elements.

## Cross-References
### Incoming
- Rendering subsystems (e.g., W3D texture loading)
- UI systems (loading menu backgrounds)
- Modding infrastructure (custom asset loading)

### Outgoing
- File I/O (FileClass)
- Surface management (BSurface)
- Palette handling (PaletteClass)

## Design Patterns
- **Facade Pattern**: Abstracts PCX file operations behind simple functions, hiding encoding/decoding complexity.
- **Dependency Injection**: Optional palette parameter allows flexible palette handling.
- **Not inferable**: No clear use of other patterns without implementation details.
