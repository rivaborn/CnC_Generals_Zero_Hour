# Generals/Code/Libraries/Source/WWVegas/WW3D2/animobj.cpp

## Purpose
Manages 3D animatable objects, including bone hierarchies, animation playback, and transform updates.

## Responsibilities
- Handles animation states (base pose, single/double/multiple anims)
- Manages bone hierarchies and transforms
- Controls animation playback (looping, ping-pong, etc.)
- Updates sub-object transforms for rendering
- Provides bone manipulation (capture/release/control)

## Key Types
- **Animatable3DObjClass (Class)**: Core class for animatable 3D objects
- **HTreeClass (Class)**: Bone hierarchy structure
- **HAnimClass (Class)**: Animation data container
- **AnimModeEnum (Enum)**: Animation playback modes (ONCE, LOOP, etc.)

## Key Functions
### `Render`
- Purpose: Updates object for rendering and progresses animations
- Calls: `Single_Anim_Progress`, `Update_Sub_Object_Transforms`

### `Set_Animation`
- Purpose: Configures animation state (single, blend, or combo)
- Calls: `Release`, asset manager functions

### `Update_Sub_Object_Transforms`
- Purpose: Recalculates transforms based on current animation state
- Calls: `Base_Update`, `Anim_Update`, `Blend_Update`, `Combo_Update`

### `Compute_Current_Frame`
- Purpose: Calculates current animation frame based on time and mode
- Calls: `WW3D::Get_Sync_Time`

### `Single_Anim_Progress`
- Purpose: Advances single animations based on elapsed time
- Calls: `Compute_Current_Frame`, `Set_Hierarchy_Valid`

## Globals
- **None**

## Dependencies
- `animobj.h`, `htree.h`, `assetmgr.h`, `hanim.h`, `hcanim.h`, `ww3d.h`, `wwmemlog.h`
- `WW3DAssetManager`, `WW3D`, `WWMath`, `WWDEBUG`
