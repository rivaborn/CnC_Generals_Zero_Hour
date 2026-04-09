# Generals/Code/Tools/WW3D/max2w3d/TARGA.H - Enhanced Analysis

## Architectural Role
This header defines the TGA image file I/O subsystem used by the WW3D (Westwood 3D) toolchain, specifically for the max2w3d converter utility. It bridges between 3D modeling tools and the game's W3D asset pipeline.

## Cross-References
### Incoming
- `max2w3d` (main converter tool) - uses Targa class for texture I/O
- Other WW3D tools - likely reference TGA structures for format compatibility

### Outgoing
- Conditionally uses `FileClass` (WWLIB) for file operations
- Falls back to standard C file I/O when `TGA_USES_WWLIB_FILE_CLASSES` is undefined

## Design Patterns
- **Adapter Pattern**: Abstracts different file I/O backends (standard C vs WWLIB)
- **Facade Pattern**: Simplifies TGA format complexity through the Targa class interface
- **Strategy Pattern**: Decode/Encode methods can be swapped for different compression schemes (implied by `IsCompressed()`)

*Not inferable*: Exact compression algorithm implementation details.
