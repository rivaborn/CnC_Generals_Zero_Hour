# Generals/Code/Tools/WW3D/max2w3d/PS2GameMtlShaderDlg.h - Enhanced Analysis

## Architectural Role
This file defines a dialog class for managing PS2-specific shader settings within the 3ds Max plugin toolchain. It bridges the gap between artist-facing UI and the W3D material pipeline, ensuring PS2 hardware limitations are enforced during asset creation.

## Cross-References
### Incoming
- Likely called by `max2w3d` exporter tools when PS2 material properties need editing
- May be referenced by other shader dialog classes (e.g., `GameMtlShaderDlg`) for preset handling

### Outgoing
- Calls into `GameMtl` for material property manipulation
- Uses `PS2ShaderBlendSettingPreset` for preset validation/comparison
- Relies on 3ds Max SDK (`<Max.h>`) for dialog management

## Design Patterns
- **Template Method**: Inherits from `GameMtlFormClass`, overriding `Dialog_Proc` while delegating common UI behavior
- **Strategy**: Preset application (`Apply_Preset`) abstracts shader configuration logic
- **Observer**: Dialog updates material state via `ReloadDialog`, suggesting a push model for UI synchronization
