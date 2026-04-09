# Generals/Code/Tools/WW3D/pluglib/iostruct.h - Enhanced Analysis

## Architectural Role
This header defines stable binary layout structures for serialization in the W3D plugin system, serving as the contract between the 3DS Max plugin tools and the W3D asset pipeline. It bridges the gap between Max's internal representation and the engine's runtime data structures.

## Cross-References
### Incoming
- `Generals/Code/Tools/WW3D/pluglib/*.cpp` (plugin tools using these structures for I/O)
- `Generals/Code/Tools/WW3D/max2w3d/*.cpp` (Max exporter using these for asset conversion)

### Outgoing
- None (pure header with no function calls)

## Design Patterns
- **Data Transfer Object (DTO)**: Structures are designed purely for serialization, decoupling in-memory representation from storage format
- **Fixed Layout**: Explicit float32 usage ensures binary compatibility across tools and platforms
- **Minimalist Design**: No behavior, only data - follows "dumb data" principle for cross-process communication

Key insight: These structures are the serialization contract for the entire W3D asset pipeline, ensuring tools like max2w3d and the engine's asset loaders speak the same binary language. The absence of functions (only structs) reinforces this as a pure data contract header.
