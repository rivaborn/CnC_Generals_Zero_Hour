# GeneralsMD/Code/Libraries/Source/WWVegas/WWAudio/AudibleSound.h

## Purpose
Defines the core audio classes for the SAGE engine, including sound objects, definitions, and playback control.

## Responsibilities
- Declares `AudibleSoundClass` and its subclasses for sound management
- Defines sound state, type, and handle management
- Provides interfaces for sound playback, volume, pan, and 3D positioning
- Declares `AudibleSoundDefinitionClass` for sound asset definitions

## Key Types
- **AudibleSoundClass (Class)**: Base class for all sound objects with playback control
- **AudibleSoundDefinitionClass (Class)**: Sound asset definition with editable properties
- **SOUND_TYPE (Enum)**: Sound type (music/sound effect)
- **SOUND_STATE (Enum)**: Playback state (stopped/playing/paused)
- **MILES_HANDLE (Type)**: Opaque handle for MILES audio system

## Key Functions
### `Play`
- Purpose: Start sound playback
- Calls: `Allocate_Miles_Handle`, `Initialize_Miles_Handle`

### `Stop`
- Purpose: Stop sound playback
- Calls: `Free_Miles_Handle`

### `Determine_Real_Volume`
- Purpose: Calculate effective volume based on settings
- Calls: None visible

### `Convert_To_Filtered`
- Purpose: Convert sound to filtered format
- Calls: None visible

## Globals
- **INVALID_MILES_HANDLE (MILES_HANDLE)**: Invalid handle constant
- **INFINITE_LOOPS (int)**: Constant for infinite looping

## Dependencies
- `mss.h` (MILES Sound System)
- `vector3.h`, `matrix3d.h` (3D math)
- `refcount.h` (reference counting)
- `rawfile.h`, `soundsceneobj.h`, `vector.h`, `wwstring.h`, `definition.h` (engine utilities)
