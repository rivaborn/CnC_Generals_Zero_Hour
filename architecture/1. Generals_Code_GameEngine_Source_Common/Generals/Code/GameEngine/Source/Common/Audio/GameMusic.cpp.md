# Generals/Code/GameEngine/Source/Common/Audio/GameMusic.cpp

## Purpose
This file manages game music, including playing and stopping tracks.

## Responsibilities
- Manages audio events for music tracks.
- Parses INI files for music track data.
- Allocates and appends audio requests to the audio system.

## Key Types
- `MusicTrack` (struct): Holds data for a music track, such as filename, volume, and ambient status.
- `MusicManager` (class): Manages playback of music tracks.

## Key Functions
### playTrack
- Purpose: Plays a specified audio event.
- Calls: `TheAudio->allocateAudioRequest`, `TheAudio->appendAudioRequest`

### stopTrack
- Purpose: Stops a specified audio track.
- Calls: `TheAudio->allocateAudioRequest`, `TheAudio->appendAudioRequest`

### addAudioEvent
- Purpose: Adds an audio event to play a music track.
- Calls: `playTrack`

### removeAudioEvent
- Purpose: Removes an audio event to stop a music track.
- Calls: `stopTrack`

## Globals
None

## Dependencies
- Key includes:
  - "Common/GameMusic.h"
  - "Common/AudioEventRTS.h"
  - "Common/AudioRequest.h"
  - "Common/GameAudio.h"
  - "Common/INI.h"
