# GeneralsMD/Code/GameEngine/Include/Common/AudioEventRTS.h

## Purpose
Defines the `AudioEventRTS` class and related types for managing audio events in the game engine.

## Responsibilities
- Encapsulates audio event properties (position, owner, volume, etc.)
- Manages audio playback state (attack, decay, looping)
- Handles localization and filename generation for audio assets
- Provides positional and object-based audio attachment

## Key Types
- **AudioEventInfo (Class)**: Not inferable.
- **OwnerType (Enum)**: Type of owner (positional, drawable, object, dead, invalid).
- **PortionToPlay (Enum)**: Audio playback portion (attack, sound, decay, done).
- **AudioPriority (Enum)**: Not inferable.
- **AudioEventRTS (Class)**: Core audio event class with playback and positioning logic.
- **DynamicAudioEventRTS (Class)**: Memory-pooled wrapper for `AudioEventRTS`.

## Key Functions
### `generateFilename`
- Purpose: Generates the filename for the audio asset.
- Calls: `adjustForLocalization`

### `generatePlayInfo`
- Purpose: Generates attack/decay sound info and playback parameters.
- Calls: Not inferable.

### `getCurrentPosition`
- Purpose: Retrieves the current position based on owner type.
- Calls: Not inferable.

### `generateFilenamePrefix`
- Purpose: Generates the directory path for audio assets.
- Calls: `adjustForLocalization`

## Globals
- None

## Dependencies
- `Common/AsciiString.h`
- `Common/GameAudio.h`
- `Common/GameMemory.h`
- `Common/GameType.h`
- `AudioEventInfo` (forward-declared)
- `AudioHandle`, `ObjectID`, `DrawableID`, `Coord3D`, `TimeOfDay`, `Real`, `Bool`, `Int` (from `GameType.h`)
