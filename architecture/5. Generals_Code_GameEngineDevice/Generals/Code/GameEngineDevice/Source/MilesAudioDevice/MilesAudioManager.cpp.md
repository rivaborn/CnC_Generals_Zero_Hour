# Generals/Code/GameEngineDevice/Source/MilesAudioDevice/MilesAudioManager.cpp

## Purpose
Implements the MilesAudioManager class, which interfaces with the Miles Sound System for audio playback in the game.

## Responsibilities
- Manages audio device initialization and shutdown
- Handles 2D/3D sound playback and streaming
- Implements audio caching and memory management
- Provides debug displays for audio state
- Manages audio event playback and completion callbacks

## Key Types
- `MilesAudioManager` (Class): Main audio manager handling Miles Sound System integration
- `AudioFileCache` (Class): Manages audio file caching and memory usage
- `INFINITE_LOOP_COUNT` (Enum): Constant for infinite loop count (1,000,000)
- `OpenAudioFile` (Struct): Represents an open audio file with metadata

## Key Functions
### `addAudioEvent`
- Purpose: Adds an audio event to the manager (debug version)
- Calls: `AudioManager::addAudioEvent`

### `audioDebugDisplay`
- Purpose: Displays audio system debug information
- Calls: `AIL_MSS_version`, `TheTacticalView->getPosition`, `TheTerrainLogic->getGroundHeight`, `AIL_get_timer_highest_delay`

### `friend_forcePlayAudioEventRTS`
- Purpose: Forces playback of an audio event
- Calls: `getInfoForAudioEvent`, `AIL_quick_load_and_play`, `AIL_quick_set_volume`

### `setSampleCompleted`
- Purpose: Callback for sample completion
- Calls: `TheAudio->notifyOfAudioCompletion`

### `streamingFileOpen`
- Purpose: Opens a file for streaming
- Calls: `TheFileSystem->openFile`

## Globals
- `AILCALLBACK` (multiple): Callback functions for Miles Sound System events
- `TheAudio` (MilesAudioManager*): Global audio manager instance

## Dependencies
- Miles Sound System (AIL)
- DirectSound (dsound.h)
- Game engine components (AudioManager, AudioFileCache)
- File system and audio event classes
- Debug display and game logic interfaces
