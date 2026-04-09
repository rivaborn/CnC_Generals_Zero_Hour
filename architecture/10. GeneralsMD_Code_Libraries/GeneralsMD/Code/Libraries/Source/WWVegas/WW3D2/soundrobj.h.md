# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/soundrobj.h

## Purpose
Defines classes for managing sound effects in the 3D world, tying sounds to render objects and handling their playback lifecycle.

## Responsibilities
- Manages sound playback tied to render objects
- Handles sound visibility/state synchronization
- Provides serialization for sound definitions
- Integrates with the prototype/loader system

## Key Types
- **SoundRenderObjClass (class)**: Render object that triggers and manages sound playback
- **SoundRenderObjDefClass (class)**: Definition/serialization class for sound render objects
- **SoundRenderObjPrototypeClass (class)**: Prototype class for sound render objects
- **SoundRenderObjLoaderClass (class)**: Loader for sound render object chunks
- **FLAGS (enum)**: Sound object behavior flags (e.g., stop when hidden)

## Key Functions
### `Set_Sound`
- Purpose: Assigns an audible sound definition to the render object
- Calls: None visible

### `On_Frame_Update`
- Purpose: Updates sound state based on object visibility
- Calls: `Update_On_Visibilty`

### `Update_On_Visibilty`
- Purpose: Handles sound playback state changes when visibility changes
- Calls: Not inferable

### `Load_W3D`/`Save_W3D`
- Purpose: Serialization methods for sound definitions
- Calls: Chunk loading/saving methods

## Globals
- **_SoundRenderObjLoader (SoundRenderObjLoaderClass)**: Global loader instance

## Dependencies
- `rendobj.h`, `wwstring.h`, `proto.h`, `w3d_file.h`, `w3derr.h`, `audiblesound.h`
- `ChunkSaveClass`, `ChunkLoadClass`, `AudibleSoundDefinitionClass`, `SceneClass`, `Matrix3D`, `Vector3`
