# Generals/Code/GameEngineDevice/Include/MilesAudioDevice/MilesAudioManager.h

## Purpose
Header for the MilesAudioManager class, which manages audio playback using the Miles Sound System (MSS) in the SAGE engine.

## Responsibilities
- Manages audio device initialization and playback
- Handles 2D/3D audio samples and streams
- Implements audio caching and resource management
- Provides audio event playback and control
- Manages audio provider selection and configuration

## Key Types
- **AudioEventRTS (Class)**: Audio event reference.
- **PlayingAudioType (Enum)**: Audio type (sample, 3D sample, stream).
- **PlayingStatus (Enum)**: Playback status (playing, stopped, paused).
- **PlayingWhich (Enum)**: Audio segment (attack, sound, decay).
- **PlayingAudio (Struct)**: Active audio playback state.
- **ProviderInfo (Struct)**: Audio provider information.
- **OpenAudioFile (Struct)**: Open audio file metadata.
- **AudioFileCache (Class)**: Audio file caching system.
- **MilesAudioManager (Class)**: Main audio manager implementation.

## Key Functions
### `init()`
- Purpose: Initialize audio device and resources.
- Calls: `buildProviderList`, `createListener`, `initDelayFilter`, `initSamplePools`.

### `playAudioEvent(AudioEventRTS *event)`
- Purpose: Play an audio event.
- Calls: `playSample`, `playSample3D`, `playStream`.

### `update()`
- Purpose: Process audio state updates.
- Calls: `processRequestList`, `processPlayingList`, `processFadingList`, `processStoppedList`.

### `notifyOfAudioCompletion(UnsignedInt audioCompleted, UnsignedInt flags)`
- Purpose: Handle audio completion callbacks.
- Calls: `findPlayingAudioFrom`.

## Globals
- **MAXPROVIDERS (Enum)**: Maximum number of audio providers (64).

## Dependencies
- `Common/AsciiString.h`, `Common/GameAudio.h`, `MSS/MSS.h`
- MSS API (e.g., `HSAMPLE`, `H3DSAMPLE`, `HSTREAM`)
- `AudioEventRTS`, `AudioEventInfo` (external)
