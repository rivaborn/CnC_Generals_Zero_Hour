# Generals/Code/Libraries/Source/WWVegas/WW3D2/soundrobj.cpp

## Purpose
Manages sound rendering objects in the W3D engine, handling sound attachment, visibility updates, and serialization.

## Responsibilities
- Manages `SoundRenderObjClass` lifecycle (creation, destruction, sound attachment)
- Handles visibility-based sound playback control
- Serializes/deserializes sound objects via W3D chunk system
- Provides factory pattern for loading sound objects

## Key Types
- **SoundRenderObjClass (Class)**: Wraps a sound object with visibility-aware playback
- **SoundRenderObjDefClass (Class)**: Definition for serializing sound render objects
- **SoundRenderObjLoaderClass (Class)**: Factory for loading sound objects from W3D files
- **FLAGS (enum)**: Sound behavior flags (e.g., `FLAG_STOP_WHEN_HIDDEN`)

## Key Functions
### `Update_On_Visibilty`
- Purpose: Syncs sound object's scene presence with render object visibility
- Calls: `Sound->Attach_To_Object`, `Sound->Add_To_Scene`, `Sound->Remove_From_Scene`

### `Set_Sound`
- Purpose: Assigns a new sound definition to the render object
- Calls: `definition->Create()`, `Sound->Remove_From_Scene`

### `Load_W3D`
- Purpose: Deserializes sound object from W3D chunk
- Calls: `definition->Load_W3D`, `W3DNEW SoundRenderObjPrototypeClass`

## Globals
- `_SoundRenderObjLoader (SoundRenderObjLoaderClass)`: Global loader instance

## Dependencies
- `soundrobj.h`, `audiblesound.h`, `sound3d.h`, `wwaudio.h`, `ffactory.h`, `wwfile.h`, `chunkio.h`, `scene.h`
- `AudibleSoundClass`, `AudibleSoundDefinitionClass`, `SceneClass`, `RenderObjClass`
