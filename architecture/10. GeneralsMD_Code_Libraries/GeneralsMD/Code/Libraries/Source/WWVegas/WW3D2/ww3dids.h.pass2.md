# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/ww3dids.h - Enhanced Analysis

## Architectural Role
This header defines the persistence chunk IDs for WW3D's renderable objects, serving as the bridge between the W3D rendering subsystem and the WWSaveLoad library's serialization framework. It enables save/load functionality for game state by identifying which render objects need to be persisted.

## Cross-References
### Incoming
- Persistence managers for `RenderObjClass`, `LightClass`, and `DazzleClass` will include this header to use the defined chunk IDs
- Save/load code in the WWSaveLoad library references these IDs during serialization

### Outgoing
- Depends on `saveloadids.h` for the base chunk ID range (`CHUNKID_WW3D_BEGIN`)

## Design Patterns
- **Enumeration as Constants**: Uses an anonymous enum to define chunk IDs, providing type safety while allowing direct integer usage
- **Dependency Injection**: The chunk IDs are injected into the persistence framework rather than hardcoded in the save/load implementation
- **Forward Compatibility**: The comment suggests future-proofing by noting potential changes to light object persistence (asset manager vs procedural creation)
