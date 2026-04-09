# Generals/Code/GameEngine/Source/Common/Audio/AudioEventRTS.cpp

## Purpose
Handles audio events in the game, managing sound properties and playback.

## Responsibilities
- Manages audio event properties such as name, priority, volume, and position.
- Generates filenames for audio files based on event information.
- Controls audio playback, including setting and getting handles, checking if currently playing, and adjusting volume.
- Handles positional audio by updating positions of objects or drawables.

## Key Types
- `AudioEventRTS` (Class): Manages audio events with various properties and methods to control playback.

## Key Functions
### AudioEventRTS::setEventName
- Purpose: Sets the event name and clears associated info if changed.
- Calls: None

### AudioEventRTS::generateFilename
- Purpose: Generates a filename for the audio file based on event info.
- Calls: `generateFilenamePrefix`, `adjustForLocalization`

### AudioEventRTS::generatePlayInfo
- Purpose: Generates playback information such as pitch shift, volume shift, and loop count.
- Calls: `GameAudioRandomValueReal`

### AudioEventRTS::getCurrentPosition
- Purpose: Retrieves the current position of the audio event.
- Calls: `findObjectByID`, `getPosition`

## Globals
None

## Dependencies
- Key includes:
  - "Common/AudioEventRTS.h"
  - "Common/AudioEventInfo.h"
  - "Common/AudioRandomValue.h"
  - "Common/AudioSettings.h"
  - "GameLogic/GameLogic.h"
  - "GameClient/Drawable.h"

- External symbols used:
  - `TheAudio`
  - `TheGameLogic`
  - `TheGameClient`
