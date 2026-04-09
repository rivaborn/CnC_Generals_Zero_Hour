# Generals/Code/Tools/WW3D/max2w3d/GameMtlShaderDlg.cpp

## Purpose
Handles shader settings UI for material editing in the Max2W3D tool.

## Responsibilities
- Manages shader blend presets and their application
- Updates material properties based on UI input
- Compares current shader settings to presets
- Reloads dialog controls with current material state

## Key Types
- **ShaderBlendSettingPreset (Struct)**: Defines preset shader blend settings (src/dest blend, depth mask, alpha test)

## Key Functions
### GameMtlShaderDlg::Apply_Preset
- Purpose: Applies a preset shader configuration to the material
- Calls: TheMtl->Set_Src_Blend, TheMtl->Set_Dest_Blend, TheMtl->Set_Depth_Mask, TheMtl->Set_Alpha_Test, TheMtl->Notify_Changed, ReloadDialog

### GameMtlShaderDlg::Set_Preset
- Purpose: Determines which preset matches the current material shader settings
- Calls: CompareShaderToBlendPreset

### GameMtlShaderDlg::CompareShaderToBlendPreset
- Purpose: Compares current shader settings against a preset
- Calls: TheMtl->Get_Src_Blend, TheMtl->Get_Dest_Blend, TheMtl->Get_Depth_Mask, TheMtl->Get_Alpha_Test

### GameMtlShaderDlg::Set_Advanced_Defaults
- Purpose: Resets advanced shader settings to defaults
- Calls: TheMtl->Set_Pri_Gradient, TheMtl->Set_Sec_Gradient, TheMtl->Set_Depth_Compare, TheMtl->Set_Detail_Color_Func, TheMtl->Set_Detail_Alpha_Func, TheMtl->Notify_Changed, ReloadDialog

## Globals
- **_ShaderBlendSettingPresetNames (char**)**: Array of preset names for UI display
- **ShaderBlendSettingPresets (ShaderBlendSettingPreset[])**: Array of predefined shader blend presets

## Dependencies
- GameMtlShaderDlg.h, GameMtlDlg.h, GameMtl.h, resource.h
- W3D shader constants (W3DSHADER_*)
