# GeneralsMD/Code/GameEngine/Source/Common/Audio/GameAudio.cpp

## Purpose
Manages audio functionality in the game, including sound, music, and speech playback, as well as audio settings and listener positioning.

## Responsibilities
- Initializes and manages audio devices and settings
- Handles audio event playback and request processing
- Manages listener position and orientation for 3D audio
- Loads and parses audio configuration from INI files
- Provides audio state management (volume, focus handling)

## Key Types
- **AudioManager (Class)**: Main audio system singleton handling all audio operations
- **AudioSettings (Class)**: Stores audio configuration parameters
- **AudioRequest (Class)**: Represents pending audio playback requests
- **AudioEventRTS (Class)**: Audio event data structure
- **AudioEventInfo (Class)**: Information about specific audio events

## Key Functions
### `init()`
- Purpose: Initializes audio system and loads configuration
- Calls: `INI::load()`, `MusicManager::new()`, `SoundManager::new()`

### `update()`
- Purpose: Updates listener position and audio effects based on game state
- Calls: `TheTacticalView->getPosition()`, `TheTerrainLogic->getGroundHeight()`

### `setVolume()`
- Purpose: Adjusts audio volume for different audio types
- Calls: None directly visible

### `parseSpeakerType()`
- Purpose: Parses speaker type configuration from INI files
- Calls: `INI::parseAsciiString()`, `AudioManager::translateSpeakerTypeToUnsignedInt()`

## Globals
- **TheSpeakerTypes (const char**)**: Array of speaker type names
- **TheSpeakerTypesCount (Int)**: Count of speaker types
- **audioSettingsFieldParseTable (FieldParse)**: Parse table for audio settings
- **TheAudio (AudioManager**)**: Global audio manager singleton

## Dependencies
- Key includes: `GameAudio.h`, `AudioAffect.h`, `AudioEventRTS.h`, `INI.h`, `FileSystem.h`
- External symbols: `TheFileSystem`, `TheTacticalView`, `TheTerrainLogic`, `ThePlayerList`, `TheControlBar`, `TheGameLogic`
