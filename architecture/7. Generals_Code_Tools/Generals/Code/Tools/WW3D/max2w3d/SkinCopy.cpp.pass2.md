# Generals/Code/Tools/WW3D/max2w3d/SkinCopy.cpp - Enhanced Analysis

## Architectural Role
This file is part of the W3D export pipeline, specifically handling skinning data migration between 3DS Max objects. It bridges the gap between Max's modifier stack and the W3D skinning system, ensuring proper skin binding preservation during model export.

## Cross-References
### Incoming
- **SceneSetup MAXScript**: Calls `wwFindSkinNode`, `wwCopySkinInfo`, and `wwDuplicateSkinWSM` for scene preparation
- **W3D export tools**: Likely invokes `copy_skin_info` during model processing

### Outgoing
- **MAX SDK**: Uses `INode`, `IDerivedObject`, and `Modifier` classes extensively
- **Skin system**: Interfaces with `SkinModifierClass` and `SkinWSMObjectClass`
- **Utility functions**: Relies on `Set_W3D_Name` and other W3D-specific helpers

## Design Patterns
- **Adapter Pattern**: Converts between Max's modifier system and W3D's skinning format
- **Factory Pattern**: Creates new `SkinModifierClass` instances with copied settings
- **Visitor Pattern**: Recursively traverses node hierarchies in `find_equivalent_node`

*Not inferable*: Exact memory management strategy for `ModContext` duplication.
