# Generals/Code/Tools/WW3D/max2w3d/GameMtlShaderDlg.cpp - Enhanced Analysis

## Architectural Role
This file implements the shader configuration UI for the Max2W3D material editor tool, bridging between the Windows dialog system and the W3D material system. It handles preset management and shader parameter synchronization.

## Cross-References
### Incoming
- **GameMtlDlg.cpp**: Likely instantiates this dialog class for material editing
- **GameMtl.cpp**: Provides the material interface (TheMtl) that this dialog manipulates

### Outgoing
- **GameMtl.h**: Uses material property getters/setters
- **resource.h**: For dialog resource IDs
- **W3D shader constants**: Directly references W3DSHADER_* defines

## Design Patterns
- **Strategy Pattern**: Preset system allows swapping different shader configurations
- **Observer Pattern**: Uses Notify_Changed() to signal material updates
- **Template Method**: Dialog_Proc handles Windows messages with specialized behavior

**Key Insight**: The preset system (8 predefined blends) shows early optimization for artist workflow - common shader setups are pre-configured rather than requiring manual parameter tweaking. The "Custom" preset (index 8) indicates this was designed for both quick setup and fine-tuning.
