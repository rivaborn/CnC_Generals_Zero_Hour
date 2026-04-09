# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/animobj.cpp

## Purpose
Manages 3D animatable objects, including bone hierarchies, animation playback, and rendering.

## Responsibilities
- Handles animation states (single, blended, combo)
- Manages bone transforms and hierarchy updates
- Controls animation playback (looping, ping-pong, etc.)
- Triggers embedded animation sounds
- Provides bone manipulation and querying

## Key Types
- `Animatable3DObjClass` (Class): Core animatable object with bone hierarchy and animation support
- `HTreeClass` (Class): Bone hierarchy structure
- `HAnimClass` (Class): Animation motion data
- `AnimComboClass` (Class): Animation combination data

## Key Functions
### `Render`
- Purpose: Updates object for rendering and advances animations
- Calls: `Single_Anim_Progress`, `Update_Sub_Object_Transforms`

### `Set_Animation`
- Purpose: Configures animation state (single, blended, or combo)
- Calls: `Release`, `Add_Ref` (on motion objects)

### `Update_Sub_Object_Transforms`
- Purpose: Recalculates bone transforms based on current animation state
- Calls: `Base_Update`, `Anim_Update`, `Blend_Update`, `Combo_Update`

### `Compute_Current_Frame`
- Purpose: Calculates current animation frame based on time and mode
- Calls: `WW3D::Get_Sync_Time`

### `Single_Anim_Progress`
- Purpose: Advances single animation frame based on time
- Calls: `Compute_Current_Frame`

## Globals
- None

## Dependencies
- `animobj.h`, `htree.h`, `assetmgr.h`, `hanim.h`, `hcanim.h`, `ww3d.h`, `wwmemlog.h`, `animatedsoundmgr.h`
- `WW3DAssetManager`, `WW3D`, `AnimatedSoundMgrClass`, `WWMath`, `WWDEBUG_SAY`, `WWASSERT`, `WWMEMLOG`
