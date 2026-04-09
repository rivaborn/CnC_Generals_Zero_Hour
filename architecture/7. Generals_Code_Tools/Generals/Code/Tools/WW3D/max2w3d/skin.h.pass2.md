# Generals/Code/Tools/WW3D/max2w3d/skin.h - Enhanced Analysis

## Architectural Role
This file defines the core classes for Westwood's skin modifier plugin in 3ds Max, bridging the asset pipeline between Max and the W3D format used by the SAGE engine. It handles bone-based deformation, vertex weighting, and UI integration for character/vehicle rigging.

## Cross-References
### Incoming
- `max2w3d` toolchain (likely calls `Get_Skin_Mod_Desc`/`Get_Skin_Obj_Desc` during plugin registration)
- Max SDK (uses `ClassDesc` for plugin system integration)

### Outgoing
- **Max SDK**: `IObjParam`, `Modifier`, `WSMObject` (base classes)
- **Internal**: `simpmod.h`, `simpobj.h` (custom base classes), `bpick.h` (bone picking)

## Design Patterns
- **Plugin Architecture**: Uses Max's `ClassDesc` system for extensibility.
- **Reference Target**: Manages object references via `RefTargetHandle` for serialization.
- **Observer**: `NotifyRefChanged` for dependency tracking (Max SDK pattern).

*Not inferable*: Exact vertex-weighting algorithm or W3D export logic.
