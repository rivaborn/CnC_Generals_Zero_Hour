# Generals/Code/Tools/ImagePacker/Include/ImagePacker.h - Enhanced Analysis

## Architectural Role
This header defines the core tool for texture atlas generation in the SAGE engine's asset pipeline. It bridges the gap between raw image assets and runtime texture resources, ensuring efficient packing and INI file generation for W3D rendering.

## Cross-References
### Incoming
- **Asset Pipeline Tools**: Likely called by build scripts or editor tools to process image directories
- **W3D Renderer**: TexturePage output feeds directly into the rendering system's texture management
- **INI System**: Generated INI files integrate with the engine's configuration infrastructure

### Outgoing
- **Image Loading**: Uses Targa class for image header parsing
- **Directory Traversal**: Relies on ImageDirectory for recursive file scanning
- **Bit Manipulation**: Uses external BitSet/BitClear utilities for flag management

## Design Patterns
- **Singleton**: Global TheImagePacker instance suggests tool-wide access pattern
- **Facade**: Encapsulates complex packing logic behind simple process() interface
- **Strategy**: Gap methods (EXTEND_RGB/GUTTER) implement different spacing strategies

*Not inferable*: Exact packing algorithm implementation details remain hidden in .cpp
