# Generals/Code/Tools/WW3D/max2w3d/util.h - Enhanced Analysis

## Architectural Role
This header provides utility functions for the 3ds Max to W3D exporter tool, bridging the gap between Max's scene graph and the W3D format's requirements. It handles naming conventions, path manipulation, and scene hierarchy queries that are critical for model export.

## Cross-References
### Incoming
- `max2w3d.cpp` (main exporter tool) - Uses all utility functions for model processing
- `skin.cpp` - Likely uses `Is_Origin` and `Find_Origin` for skin attachment points
- `nodelist.cpp` - Uses `Append_Lod_Character` for LOD management

### Outgoing
- Directly interacts with 3ds Max SDK (`<Max.h>`) for node operations
- Uses `skin.h` and `nodelist.h` for scene hierarchy traversal

## Design Patterns
- **Utility Class Pattern**: Functions are stateless utilities grouped in a header
- **Naming Convention Enforcer**: `Set_W3D_Name` and `Split_Node_Name` enforce W3D-specific naming rules
- **Path Manipulation Helper**: `Create_Full_Path`/`Create_Relative_Path` abstract filesystem operations

*Not inferable*: No clear use of creational or behavioral patterns in this header-only file.
