# GeneralsMD/Code/GameEngine/Include/Common/GameMusic.h

## Purpose
Defines music-related classes and interfaces for the game audio system.

## Responsibilities
- Declares `MusicTrack` for storing music track metadata
- Defines `MusicManager` for managing music playback
- Provides memory pool management for `MusicTrack` objects
- Exposes methods for track control (play/stop) and event management

## Key Types
- **MusicTrack (Class)**: Holds metadata for a music track (index, name, filename, volume, etc.)
- **MusicManager (Class)**: Manages music playback and event handling
- **MusicTrackMagicEnum (Enum)**: Not inferable (likely unused placeholder)
- **MusicTrack_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely unused placeholder)
- **AudioEventRTS (Class)**: Forward-declared audio event type
- **FieldParse (Struct)**: Forward-declared INI parsing structure

## Key Functions
### MusicTrack::MusicTrack()
- Purpose: Constructs a `MusicTrack` object
- Calls: None

### MusicManager::playTrack()
- Purpose: Plays a music track using the specified audio event
- Calls: None (implementation not shown)

### MusicManager::stopTrack()
- Purpose: Stops a music track by its audio handle
- Calls: None (implementation not shown)

### MusicManager::addAudioEvent()
- Purpose: Adds an audio event to the manager
- Calls: None (implementation not shown)

### MusicManager::removeAudioEvent()
- Purpose: Removes an audio event from the manager
- Calls: None (implementation not shown)

### MusicManager::setVolume()
- Purpose: Sets the music volume
- Calls: None (implementation not shown)

## Globals
- **MusicTrack::m_musicTrackFieldParseTable (FieldParse[])
