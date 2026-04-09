# Generals/Code/GameEngine/Source/Common/Audio/GameSounds.cpp

## Purpose
This file contains the implementation of the `SoundManager` class, which manages audio events and sound playback in the game.

## Responsibilities
- Manages initialization and cleanup of audio resources.
- Handles adding and processing audio events.
- Controls the number of playing 2D and 3D samples.
- Determines if an audio event can be played based on various criteria such as distance, shroud status, voice limits, and priority.

## Key Types
- `SoundManager` (Class): Manages audio playback and event handling.

## Key Functions
### SoundManager::init
- Purpose: Initializes the sound manager.
- Calls: None

### SoundManager::postProcessLoad
- Purpose: Post-processes audio initialization after loading.
- Calls: None

### SoundManager::update
- Purpose: Updates the sound manager state.
- Calls: None

### SoundManager::reset
- Purpose: Resets the sound manager's counters for playing samples.
- Calls: None

### SoundManager::addAudioEvent
- Purpose: Adds an audio event to be played.
- Calls:
  - `TheAudio->getNum2DSamples()`
  - `TheAudio->getNum3DSamples()`
  - `canPlayNow(eventToAdd)`
  - `TheAudio->allocateAudioRequest(true)`
  - `audioRequest->m_pendingEvent = eventToAdd`
  - `audioRequest->m_request = AR_Play`
  - `TheAudio->appendAudioRequest(audioRequest)`
  - `TheAudio->releaseAudioEventRTS(eventToAdd)`

### SoundManager::canPlayNow
- Purpose: Determines if an audio event can be played based on various criteria.
- Calls:
  - `event->isPositionalAudio()`
  - `BitTest(event->getAudioEventInfo()->m_type, ST_GLOBAL)`
  - `TheAudio->getListenerPosition()`
  - `distance.sub(pos)`
  - `distance.length()`
  - `ThePartitionManager->getShroudStatusForPlayer(localPlayerNdx, pos)`
  - `violatesVoice(event)`
  - `isInterrupting(event)`
  - `TheAudio->doesViolateLimit(event)`
  - `TheAudio->isPlayingLowerPriority(event)`

## Globals
- None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Lib/Basetype.h"
  - "Common/GameSounds.h"
  - "Common/AudioEventInfo.h"
  - "Common/AudioEventRTS.h"
  - "Common/AudioRequest.h"
  - "Common/Player.h"
  - "Common/PlayerList.h"
  - "GameLogic/PartitionManager.h"

- External symbols used:
  - `TheAudio`
  - `ThePlayerList`
  - `ThePartitionManager`
