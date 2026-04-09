# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/soundrobj.cpp

## Purpose
Manages sound rendering objects in the W3D engine, handling sound attachment, visibility updates, and serialization.

## Responsibilities
- Manages sound objects attached to render objects
- Handles visibility-based sound playback control
- Serializes/deserializes sound render objects
- Updates sound state on frame updates

## Key Types
- **SoundRenderObjClass (Class)**: Manages sound playback tied to a render object
- **SoundRenderObjDefClass (Class)**: Definition class for serializing sound render objects
- **SoundRenderObjLoaderClass (Class)**: Loads sound render objects from W3D files
- **FLAGS (enum)**: Sound object flags (e.g., FLAG_STOP_WHEN_HIDDEN)

## Key Functions
### Set_Sound
- Purpose: Assigns a sound definition to the render object
- Calls: REF_PTR_RELEASE, definition->Create()

### Update_On_Visibilty
- Purpose: Updates sound playback based on object visibility
- Calls: Validate_Transform, Sound->Attach_To_Object, Sound->Add_To_Scene, Sound->Remove_From_Scene

### Load_W3D
- Purpose: Loads sound render object definitions from W3D chunks
- Calls: definition->Load_W3D, W3DNEW

## Globals
- **_SoundRenderObjLoader (SoundRenderObjLoaderClass)**: Global loader instance

## Dependencies
- audiblesound.h, sound3d.h, wwaudio.h, ffactory.h, wwfile.h, chunkio.h, scene.h
- WW3DErrorType, ChunkLoadClass, ChunkSaveClass, AudibleSoundDefinitionClass, AudibleSoundClass
