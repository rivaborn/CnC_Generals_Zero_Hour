# Generals/Code/Tools/WW3D/max2w3d/presetexportoptionsdialog.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI layer for the Max2W3D export tool's preset configuration system, bridging between the 3DS Max plugin interface and the W3D export pipeline. It enforces preset-specific constraints while maintaining compatibility with the broader asset pipeline.

## Cross-References
### Incoming
- Called by Max2W3D plugin when user invokes export with presets
- Used by W3D export system to validate preset configurations

### Outgoing
- Configures `W3dExportClass` through `w3dexp.h`
- Launches `AnimationCompressionSettingsDialogClass` for advanced compression options
- Interacts with Max SDK interfaces (`ICustEdit`, `ISpinnerControl`)

## Design Patterns
- **Bridge Pattern**: Decouples preset-specific constraints from UI implementation
- **Command Pattern**: Encapsulates export settings as a command object (`PresetExportOptionsDialogClass`)
- **Template Method**: `Save_Settings` enforces preset rules while allowing UI flexibility

*Not inferable*: Exact relationship with W3D serialization pipeline.
