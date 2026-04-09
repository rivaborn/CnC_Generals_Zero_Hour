# Generals/Code/Tools/WW3D/max2w3d/PS2GameMtlShaderDlg.h

## Purpose
Defines a dialog class for managing PS2 shader settings in a 3D modeling tool.

## Responsibilities
- Manages shader settings for PS2 GameMtl materials
- Provides preset application and comparison functionality
- Handles dialog activation and reloading
- Inherits from GameMtlFormClass for base UI functionality

## Key Types
- **GameMtl (Class)**: Base material class for the game
- **PS2ShaderBlendSettingPreset (Struct)**: Preset configuration for shader blending
- **PS2GameMtlShaderDlg (Class)**: Dialog class for shader settings management

## Key Functions
### PS2GameMtlShaderDlg/Dialog_Proc
- Purpose: Handles Windows dialog messages for the shader settings dialog
- Calls: Not inferable

### PS2GameMtlShaderDlg/Apply_Preset
- Purpose: Applies a shader preset to the current material
- Calls: Not inferable

### PS2GameMtlShaderDlg/Set_Preset
- Purpose: Sets the current shader preset
- Calls: Not inferable

### PS2GameMtlShaderDlg/CompareShaderToBlendPreset
- Purpose: Compares current shader settings to a preset
- Calls: Not inferable

### PS2GameMtlShaderDlg/Set_Advanced_Defaults
- Purpose: Sets advanced shader settings to default values
- Calls: Not inferable

## Globals
- None

## Dependencies
- `<Max.h>`: 3ds Max SDK headers
- `GameMtlForm.h`: Base form class for material dialogs
- `GameMtl`: Material class definition
- `PS2ShaderBlendSettingPreset`: Preset structure definition
