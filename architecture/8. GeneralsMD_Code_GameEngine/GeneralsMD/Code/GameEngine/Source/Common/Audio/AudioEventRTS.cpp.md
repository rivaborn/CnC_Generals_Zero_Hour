# GeneralsMD/Code/GameEngine/Source/Common/Audio/AudioEventRTS.cpp

## Purpose
Implements the AudioEventRTS class, handling audio event management for the game.

## Responsibilities
- Manages audio event construction, copying, and destruction
- Handles audio event state (position, priority, volume, etc.)
- Generates filenames and play info for audio assets
- Tracks audio playback state and handles delays/loops

## Key Types
- **AudioEventRTS (Class)**: Represents an audio event with properties like name, priority, volume, and spatial positioning
- **AudioEventInfo (Pointer)**: Reference to audio event metadata
- **OwnerType (Enum)**: Tracks audio owner type (object, drawable, position, etc.)

## Key Functions
### `generateFilename`
- Purpose: Constructs the filename for an audio asset based on event info
- Calls: `generateFilenamePrefix`, `generateFilenameExtension`, `adjustForLocalization`

### `generatePlayInfo`
- Purpose: Sets up playback parameters like pitch, volume, and loop count
- Calls: `GameAudioRandomValueReal`

### `getCurrentPosition`
- Purpose: Retrieves the current 3D position for positional audio
- Calls: `TheGameLogic->findObjectByID`, `TheGameClient->findDrawableByID`

### `isPositionalAudio`
- Purpose: Determines if the audio event should be positional
- Calls: None (uses member variables)

## Globals
- **TheAudio (External)**: Audio system interface
- **TheGameLogic (External)**: Game logic system
- **TheGameClient (External)**: Client-side game system
- **TheFileSystem (External)**: File system utilities

## Dependencies
- Common/AudioEventRTS.h (header)
- Common/AudioEventInfo.h
- Common/AudioRandomValue.h
- Common/AudioSettings.h
- GameLogic/GameLogic.h
- GameLogic/LogicRandomValue.h
- GameClient/Drawable.h
- GameClient/GameClient.h
