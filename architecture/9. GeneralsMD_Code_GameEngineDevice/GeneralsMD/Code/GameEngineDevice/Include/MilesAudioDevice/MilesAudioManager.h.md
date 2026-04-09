# GeneralsMD/Code/GameEngineDevice/Include/MilesAudioDevice/MilesAudioManager.h

## Purpose
Header for the MilesAudioManager class, which manages audio playback using the Miles Sound System (MSS) in the SAGE engine.

## Responsibilities
- Manages audio device initialization and playback
- Handles 2D/3D audio samples and streams
- Implements audio event management and caching
- Provides audio debugging and diagnostics

## Key Types
- **AudioEventRTS (Class)**: Audio event reference.
- **PlayingAudioType (Enum)**: Audio type (sample, 3D sample, stream).
- **PlayingStatus (Enum)**: Playback state (playing, stopped, paused).
- **PlayingWhich (Enum)**: Audio segment type (attack, sound, decay).
- **PlayingAudio (Struct)**: Active audio playback state.
- **ProviderInfo (Struct)**: Audio provider metadata.
- **OpenAudioFile (Struct)**: Open file tracking for caching.
- **AudioFileCache (Class)**: Manages audio file caching.
- **MilesAudioManager (Class)**: Core audio manager implementing AudioManager.

## Key Functions
### `init()`
- Purpose: Initialize audio device and resources.
- Calls: `buildProviderList`, `createListener`, `initDelayFilter`, `initSamplePools`.

### `playAudioEvent(AudioEventRTS *event)`
- Purpose: Play an audio event.
- Calls: `playSample`, `playSample3D`, `playStream`.

### `processRequestList()`
- Purpose: Process pending audio requests.
- Calls: `shouldProcessRequestThisFrame`, `adjustRequest`, `checkForSample`.

### `notifyOfAudioCompletion(UnsignedInt audioCompleted, UnsignedInt flags)`
- Purpose: Handle audio completion callbacks.
- Calls: `findPlayingAudioFrom`.

### `killLowestPrioritySoundImmediately(AudioEventRTS *event)`
- Purpose: Stop lowest-priority audio for resource management.
- Calls: `findLowestPrioritySound`.

## Globals
- **MAXPROVIDERS (Enum)**: Maximum audio providers (64).
- **m_provider3D (ProviderInfo[MAXPROVIDERS])**: 3D audio provider list.
- **m_digitalHandle (HDIGDRIVER)**: Digital audio device handle.
- **m_listener (H3DPOBJECT)**: 3D audio listener object.

## Dependencies
- `Common/AsciiString.h`, `Common/GameAudio.h`, `MSS/MSS.h`
- MSS API (e.g., `HSAMPLE`, `H3DSAMPLE`, `HSTREAM`)
- `AudioEventRTS`, `AudioEventInfo`, `AudioRequest`
