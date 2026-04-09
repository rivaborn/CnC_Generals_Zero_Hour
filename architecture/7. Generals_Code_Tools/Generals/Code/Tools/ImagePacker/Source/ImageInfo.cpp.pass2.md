# Generals/Code/Tools/ImagePacker/Source/ImageInfo.cpp - Enhanced Analysis

## Architectural Role
This file defines the `ImageInfo` class, which serves as a data container for image metadata during the texture packing process in the ImagePacker tool. It bridges the gap between raw image files and the packed texture atlas system used by the W3D renderer.

## Cross-References
### Incoming
- Likely called by `ImagePacker` tool components that manage texture atlas generation
- Used by packing algorithms that arrange images on texture pages

### Outgoing
- Relies on standard C++ memory management (`delete []`)
- No external subsystem calls detected (tool-specific utility class)

## Design Patterns
- **Data Transfer Object (DTO)**: Encapsulates image metadata for passing between packing stages
- **Resource Management**: Explicit memory cleanup in destructor for dynamically allocated strings
- **Linked List**: Maintains `nextPageImage`/`prevPageImage` pointers for image ordering on pages

*Not inferable*: No clear use of Factory, Observer, or other patterns from this file alone.
