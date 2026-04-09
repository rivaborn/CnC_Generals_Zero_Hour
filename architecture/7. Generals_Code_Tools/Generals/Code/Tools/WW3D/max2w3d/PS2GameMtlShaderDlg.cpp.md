# Generals/Code/Tools/WW3D/max2w3d/PS2GameMtlShaderDlg.cpp

## Purpose
Handles the PS2-specific shader blend settings dialog for material editing in the max2w3d tool.

## Responsibilities
- Manages PS2 shader blend presets (opaque, additive, alpha blend, etc.)
- Updates material properties based on user selections
- Compares current settings against predefined presets
- Synchronizes UI with material state

## Key Types
- **PS2ShaderBlendSettingPreset (struct)**: Stores PS2 shader blend parameters (A, B, C, D, depth mask, alpha test)

## Key Functions
### PS2GameMtlShaderDlg::Dialog_Proc
- Purpose: Handles dialog messages and user input
- Calls: `Apply_Preset`, `Set_Preset`, `TheMtl->Set_*`, `ReloadDialog`

### PS2GameMtlShaderDlg::Apply_Preset
- Purpose: Applies a preset shader configuration to the material
- Calls: `TheMtl->Set_*`, `ReloadDialog`, `TheMtl->Compute_PC_Shader_From_PS2_Shader`

### PS2GameMtlShaderDlg::Set_Preset
- Purpose: Updates the preset combo box based on current material settings
- Calls: `CompareShaderToBlendPreset`, `TheMtl->Compute_PC_Shader_From_PS2_Shader`

### PS2GameMtlShaderDlg::CompareShaderToBlendPreset
- Purpose: Checks if current settings match a preset
- Calls: `TheMtl->Get_*`

## Globals
- **_PS2ShaderBlendSettingPresetNames (char**)**: Array of preset names
- **PS2ShaderBlendSettingPresets (PS2ShaderBlendSettingPreset[])**: Predefined shader blend presets

## Dependencies
- `PS2GameMtlShaderDlg.h`, `GameMtlDlg.h`, `GameMtl.h`, `resource.h`
- `W3DSHADER_*` constants (depth mask, alpha test flags)
- `PSS_*` constants (shader parameters)
