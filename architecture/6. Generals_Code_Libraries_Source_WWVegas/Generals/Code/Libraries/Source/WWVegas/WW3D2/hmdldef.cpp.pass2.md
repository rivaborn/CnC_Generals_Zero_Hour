# Generals/Code/Libraries/Source/WWVegas/WW3D2/hmdldef.cpp - Enhanced Analysis

## Architectural Role
This file implements the core hierarchical model loading system for the W3D format, serving as the bridge between the file I/O subsystem and the rendering pipeline. It handles version compatibility and memory management for skeletal models used throughout the game.

## Cross-References
### Incoming
- Rendering system (uses loaded models)
- Animation system (depends on hierarchy data)
- Mod loading infrastructure (for custom models)

### Outgoing
- `ChunkLoadClass` (file I/O)
- `SnapPointsClass` (attachment points)
- Memory allocation system (`W3DNEWARRAY`)

## Design Patterns
- **Resource Management**: Uses explicit `Free()` pattern for deterministic cleanup
- **Version Adapter**: Handles pre-3.0 format differences via conditional logic
- **Composite**: Manages collection of sub-objects as part of hierarchical structure

*Not inferable*: No clear use of Factory, Observer, or other patterns in this file alone.
