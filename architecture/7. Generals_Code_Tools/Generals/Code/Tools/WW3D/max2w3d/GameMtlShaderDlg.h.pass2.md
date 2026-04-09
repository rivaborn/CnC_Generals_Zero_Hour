# Generals/Code/Tools/WW3D/max2w3d/GameMtlShaderDlg.h - Enhanced Analysis

## Architectural Role
This header defines the shader dialog interface for the Max2W3d exporter tool, bridging 3ds Max's material system with the game's W3D shader pipeline. It's part of the asset pipeline tooling that enables artists to configure shaders for in-game use.

## Cross-References
### Incoming
- `GameMtlForm.h` (base class)
- `PS2GameMtlShaderDlg.h` (platform-specific subclass)

### Outgoing
- 3ds Max SDK (`<Max.h>`)
- `GameMtl` class (material system)
- `ShaderBlendSettingPreset` struct (shader presets)

## Design Patterns
- **Template Method**: `Dialog_Proc` handles generic dialog messages while allowing subclasses to override specific behavior.
- **Strategy**: Preset application (`Apply_Preset`) abstracts shader configuration logic.
- **Observer**: Dialog activation/deactivation suggests event-driven UI updates.
