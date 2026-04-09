# Generals/Code/Tools/WW3D/max2w3d/w3dappdata.cpp - Enhanced Analysis

## Architectural Role
This file serves as the bridge between 3DS Max's scene graph and the W3D export pipeline, encapsulating metadata about how each node should be processed during export. It's critical for the asset pipeline, ensuring consistent conversion of artist-created content into the engine's optimized format.

## Cross-References
### Incoming
- `max2w3d` exporter tools (e.g., `max2w3d.cpp`) - calls node property checkers
- W3D export pipeline - uses app data structures during W3D file generation
- Max plugin UI - likely references these functions for property display

### Outgoing
- **W3DAppData2Struct** - core class for storing export metadata
- **W3DDazzleAppDataStruct** - specialized dazzle effect data
- **3DS Max SDK** - for node inspection (e.g., `INode`, `WSM_DERIVOB_CLASS_ID`)

## Design Patterns
- **Adapter Pattern**: Wraps Max node properties in W3D-specific structures
- **Strategy Pattern**: Different geometry/collision types are selected via flags
- **Facade Pattern**: Simplifies complex Max SDK calls behind clean interfaces

*Not inferable*: Exact relationship with W3D runtime collision systems.
