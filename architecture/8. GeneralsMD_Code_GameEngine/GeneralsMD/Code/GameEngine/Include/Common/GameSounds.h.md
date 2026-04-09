# GeneralsMD/Code/GameEngine/Include/Common/GameSounds.h

## Purpose
Header file defining the `SoundManager` class, responsible for managing audio events and sound playback in the game.

## Responsibilities
- Manages 2D and 3D audio samples
- Handles audio event processing and playback
- Tracks active sound samples and their completion
- Provides audio system initialization and updates
- Manages listener position and audible distance for spatial audio

## Key Types
- **AudioEventRTS (Class)**: Not inferable (forward-declared).
- **SoundManager (Class)**: Manages audio playback and sound events in the game.

## Key Functions
### SoundManager::init
- Purpose: Initializes the sounds system.
- Calls: Not inferable.

### SoundManager::update
- Purpose: Services sounds tasks.
- Calls: Not inferable.

### SoundManager::addAudioEvent
- Purpose: Adds an audio event to the sound manager.
- Calls: Not inferable.

### SoundManager::canPlayNow
- Purpose: Determines if a sound can still be played.
- Calls: `violatesVoice`, `isInterrupting`.

### SoundManager::getFilenameForPlayFromAudioEvent
- Purpose: Retrieves the filename for a sound from an audio event.
- Calls: Not inferable.

## Globals
- None.

## Dependencies
- `Common/SubsystemInterface.h`
- `Common/GameAudio.h`
- `Common/GameType.h`
- `AudioEventRTS` (forward-declared)
