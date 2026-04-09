# GeneralsMD/Code/GameEngine/Include/Common/GameAudio.h

## Purpose
Header defining the `AudioManager` class and related audio types for the game's sound system.

## Responsibilities
- Manages audio events, music, and sound playback
- Handles audio device initialization and control
- Implements sound prioritization and caching
- Provides interfaces for audio debugging and scripting

## Key Types
- **AudioManager (Class)**: Central audio subsystem managing sound/music playback
- **AudioEventRTS (Class)**: Audio event descriptor
- **AudioEventInfo (Class)**: Audio event metadata
- **AudioRequest (Class)**: Audio operation request
- **AudioSettings (Class)**: Audio configuration
- **AudioHandle (Type)**: Handle for tracking audio events
- **AudioAffect (Enum)**: Audio category flags (music, sound, etc.)
- **AudioType (Enum)**: Audio type classifications

## Key Functions
### addAudioEvent
- Purpose: Adds an audio event to the playback queue
- Calls: Internal audio processing pipeline

### removeAudioEvent
- Purpose: Stops and removes a playing audio event
- Calls: Audio cleanup routines

### update
- Purpose: Updates audio state and processes requests
- Calls: MusicManager, SoundManager updates

### shouldPlayLocally
- Purpose: Determines if audio should play based on game state
- Calls: Position/shroud checks

### setListenerPosition
- Purpose: Updates 3D audio listener position
- Calls: Device-specific position setting

## Globals
- **TheAudio (AudioManager*)**: Global audio subsystem instance

## Dependencies
- `SubsystemInterface` (inheritance)
- `AsciiString`, `Coord3D` (types)
- `MusicManager`, `SoundManager` (subsystems)
- STL containers (`list`, `vector`, `hash_map`)
