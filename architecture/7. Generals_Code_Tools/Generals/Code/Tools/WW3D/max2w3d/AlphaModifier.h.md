# Generals/Code/Tools/WW3D/max2w3d/AlphaModifier.h

## Purpose
Defines a 3DS Max modifier plugin for alpha channel manipulation in WW3D models.

## Responsibilities
- Implements a modifier class for vertex alpha channel editing
- Provides parameter block management for modifier settings
- Handles UI dialog for modifier parameters
- Manages reference targets and object modification

## Key Types
- **AlphaModifierClass (Class)**: Main modifier class for alpha channel manipulation
- **AlphaModDlgProc (Class)**: Dialog processor for the modifier's UI
- **ALPHA_MODIFIER_CLASSID (Class_ID)**: Unique identifier for the modifier

## Key Functions
### Get_Alpha_Desc
- Purpose: Returns the ClassDesc for the alpha modifier
- Calls: Not inferable

### AlphaModifierClass::ModifyObject
- Purpose: Applies alpha modifications to the target object
- Calls: Not inferable

### AlphaModifierClass::BeginEditParams
- Purpose: Initializes the modifier's parameter UI
- Calls: Not inferable

### AlphaModDlgProc::DlgProc
- Purpose: Handles dialog messages for the modifier UI
- Calls: Not inferable

## Globals
- **ALPHA_VERTEX_CHANNEL (int)**: Defines the vertex channel used for alpha (10)

## Dependencies
- `<max.h>` - 3DS Max SDK headers
- `<iparamm2.h>` - Parameter block support
- `<istdplug.h>` - Standard plugin interfaces
- `<meshadj.h>` - Mesh adjustment utilities
- `<modstack.h>` - Modifier stack support
- `<macrorec.h>` - Macro recorder support
- `<resource.h>` - Resource IDs
- `<dllmain.h>` - Plugin DLL main header
