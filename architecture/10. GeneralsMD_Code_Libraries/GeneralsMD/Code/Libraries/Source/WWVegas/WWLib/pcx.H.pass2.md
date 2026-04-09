# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/pcx.H - Enhanced Analysis

## Architectural Role
This header defines the PCX image format I/O interface, bridging the low-level file system (WWFile) with the rendering pipeline (Surface/Palette). It serves as a legacy image loader for the SAGE engine, likely used during development or for modding support.

## Cross-References
### Incoming
- Rendering systems (e.g., texture loading)
- Modding tools (custom asset import)
- Legacy asset pipeline (pre-W3D migration)

### Outgoing
- `FileClass` (WWFile) for file I/O
- `Surface` (BSurface) for image data storage
- `PaletteClass` (Palette) for color management

## Design Patterns
- **Adapter Pattern**: Converts PCX format to engine-native Surface/Palette structures
- **Factory Method**: `Read_PCX_File` constructs Surface objects dynamically
- **Resource Management**: Handles external buffers via `buff`/`size` parameters (not inferable if unused)

*Not inferable*: No clear use of Singleton or Observer patterns.
