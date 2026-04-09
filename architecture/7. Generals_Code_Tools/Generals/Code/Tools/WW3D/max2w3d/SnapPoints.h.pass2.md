# Generals/Code/Tools/WW3D/max2w3d/SnapPoints.h - Enhanced Analysis

## Architectural Role
This file is part of the 3ds Max plugin toolchain (max2w3d) responsible for converting 3D assets into the W3D format used by the SAGE engine. It bridges the 3ds Max SDK with the W3D export pipeline, specifically handling the serialization of helper points (snap points) used for model attachment and positioning in-game.

## Cross-References
### Incoming
- Likely called by the main max2w3d export pipeline (e.g., `Generals/Code/Tools/WW3D/max2w3d/Export.cpp`) during W3D model generation.
- May be referenced by other asset exporters needing snap point data.

### Outgoing
- Uses `ChunkSaveClass` (W3D chunk serialization system) to write snap point data.
- Interacts with `INode` (3ds Max scene graph node) to traverse the 3D hierarchy.

## Design Patterns
- **Static Utility Class**: `SnapPointsClass` is purely static, acting as a namespace for export functionality.
- **Visitor Pattern (Implicit)**: The `Export_Points` method traverses the scene graph (via `INode`), suggesting a visitor-like approach to asset processing.
- **Chunk-Based Serialization**: Uses `ChunkSaveClass` to write data in a structured, versioned format (common in W3D files).

*Not inferable*: No clear use of other patterns (e.g., Factory, Observer) in the header.
