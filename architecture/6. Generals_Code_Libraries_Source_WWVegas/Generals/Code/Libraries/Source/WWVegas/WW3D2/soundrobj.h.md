# Generals/Code/Libraries/Source/WWVegas/WW3D2/soundrobj.h

## Purpose
Defines classes for managing sound rendering objects in the 3D engine, including sound playback, visibility handling, and serialization.

## Responsibilities
- Manages sound playback tied to render objects
- Handles visibility-based sound triggering/stopping
- Provides serialization for sound objects via W3D chunks
- Implements prototype system for sound render objects

## Key Types
- **SoundRenderObjClass (Class)**: Core class for sound render objects that trigger/stop sounds based on visibility
- **SoundRenderObjDefClass (Class)**: Definition class for sound render objects with serialization support
- **SoundRenderObjPrototypeClass (Class)**: Prototype class for sound render objects
- **SoundRenderObjLoaderClass (Class)**: Loader class for W3D chunk loading
- **FLAGS (Enum)**: Flags for sound behavior (e.g., stop when hidden)

## Key Functions
### SoundRenderObjClass::On_Frame_Update
- Purpose: Updates sound state based on object visibility
- Calls: Update_On_Visibilty

### SoundRenderObjClass::Set_Sound
- Purpose: Assigns a sound definition to the render object
- Calls: None visible

### SoundRenderObjDefClass::Load_W3D
- Purpose: Loads sound render object definition from W3D chunk
- Calls: Read_Header, Read_Definition

### SoundRenderObjDefClass::Save_W3D
- Purpose: Saves sound render object definition to W3D chunk
- Calls: Write_Header, Write_Definition

## Globals
- **_SoundRenderObjLoader (SoundRenderObjLoaderClass)**: Global loader instance for sound render objects

## Dependencies
- Key includes: "rendobj.h", "wwstring.h", "proto.h", "w3d_file.h", "w3derr.h", "audiblesound.h"
- External symbols: ChunkSaveClass, ChunkLoadClass, AudibleSoundDefinitionClass, AudibleSoundClass, SceneClass, Matrix3D, Vector3, RenderInfoClass
