# GeneralsMD/Code/GameEngine/Source/Common/Audio/GameSounds.cpp

## Purpose
Manages game audio events, handling playback decisions and resource limits.

## Responsibilities
- Determines if audio events can play based on distance, shroud, voice limits, and channel availability
- Tracks playing 2D and 3D audio samples
- Interfaces with the audio system to queue and manage sound requests

## Key Types
- SoundManager (Class): Core audio management class handling playback decisions
- AudioEventRTS (Class): Audio event data structure (defined elsewhere)
- AudioRequest (Class): Audio request structure (defined elsewhere)

## Key Functions
### SoundManager::addAudioEvent
- Purpose: Queues an audio event for playback if resources are available
- Calls: TheAudio->allocateAudioRequest, TheAudio->appendAudioRequest, TheAudio->releaseAudioEventRTS, canPlayNow

### SoundManager::canPlayNow
- Purpose: Determines if an audio event can be played based on multiple criteria
- Calls: TheAudio->getListenerPosition, TheAudio->doesViolateLimit, TheAudio->isPlayingLowerPriority, TheAudio->isPlayingAlready, ThePartitionManager->getShroudStatusForPlayer, violatesVoice, isInterrupting

### SoundManager::violatesVoice
- Purpose: Checks if an audio event violates voice limits for an object
- Calls: TheAudio->isObjectPlayingVoice

### SoundManager::isInterrupting
- Purpose: Checks if an audio event has interrupt flags set
- Calls: None

## Globals
- None

## Dependencies
- Key includes: PreRTS.h, Basetype.h, GameSounds.h, AudioEventInfo.h, AudioEventRTS.h, AudioRequest.h, Player.h, PlayerList.h, PartitionManager.h
- External symbols: TheAudio, ThePlayerList, ThePartitionManager, DEBUG_LOG (conditional)
