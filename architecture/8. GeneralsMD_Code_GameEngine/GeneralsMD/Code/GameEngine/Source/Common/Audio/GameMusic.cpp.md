# GeneralsMD/Code/GameEngine/Source/Common/Audio/GameMusic.cpp

## Purpose
Manages music playback in the game, handling track loading, playing, and stopping via audio requests.

## Responsibilities
- Manages music tracks and their properties (filename, volume, ambient)
- Handles playback and stopping of music tracks
- Interfaces with the audio system via `AudioRequest` and `AudioEventRTS`

## Key Types
- **MusicTrack (struct)**: Stores music track properties (filename, volume, ambient)
- **MusicManager (class)**: Manages music playback and track handling

## Key Functions
### `playTrack(AudioEventRTS *eventToUse)`
- Purpose: Initiates playback of a music track via an audio request.
- Calls: `TheAudio->allocateAudioRequest`, `TheAudio->appendAudioRequest`

### `stopTrack(AudioHandle eventToRemove)`
- Purpose: Stops playback of a music track via an audio request.
- Calls: `TheAudio->allocateAudioRequest`, `TheAudio->appendAudioRequest`

### `addAudioEvent(AudioEventRTS *eventToAdd)`
- Purpose: Alias for `playTrack` to add a music event.
- Calls: `playTrack`

### `removeAudioEvent(AudioHandle eventToRemove)`
- Purpose: Alias for `stopTrack` to remove a music event.
- Calls: `stopTrack`

## Globals
- **MUSIC_PATH (const char**)**: Path to music files directory.

## Dependencies
- `Common/GameMusic.h`, `Common/AudioEventRTS.h`, `Common/AudioRequest.h`, `Common/GameAudio.h`, `Common/INI.h`
