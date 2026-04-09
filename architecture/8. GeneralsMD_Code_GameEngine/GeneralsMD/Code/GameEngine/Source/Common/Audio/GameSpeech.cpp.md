# GeneralsMD/Code/GameEngine/Source/Common/Audio/GameSpeech.cpp

## Purpose
Manages in-game speech/audio playback, including speaker management, speech queuing, and audio streaming.

## Responsibilities
- Manages speech playback via `SpeechManager` and `Speaker` classes
- Handles speech queuing, prioritization, and interruption logic
- Provides audio streaming and volume control
- Supports speech pausing, resuming, and cancellation

## Key Types
- **Speech (struct)**: Holds speech metadata (ID, name, volume, priority, etc.)
- **SpeechItem (struct)**: Represents a queued speech item with priority and timeout
- **Speaker (class)**: Manages individual audio streams and speech queues
- **SpeechManager (class)**: Core interface for speech management and speaker creation
- **Flags (enum)**: Speech item state flags (e.g., PAUSED)

## Key Functions
### `SpeechManager::init`
- Purpose: Initializes the speech system and audio device
- Calls: `deinit`, `TheAudio->device()`

### `Speaker::say`
- Purpose: Queues speech for playback with priority and timeout
- Calls: `AudioStreamerOpen`, `AudioStreamerStart`, `AudioStreamerSetVolume`

### `Speaker::update`
- Purpose: Services speech playback and queue processing
- Calls: `AudioStreamerActive`, `AudioStreamerEndTimeStamp`, `AudioStreamerPause`

### `speechFromInfo`
- Purpose: Converts `SpeechInfo` to `Speech` struct
- Calls: None (direct assignment)

### `getNextFilenameFromSpeech`
- Purpose: Generates the next speech file path from speech data
- Calls: `GameClientRandomValue`

## Globals
- **BASE_DLG_DIR (const char**)**: Base directory for speech files
- **BASE_DLG_EXT (const char**)**: Speech file extension (".wav")
- **NUM_DLG_PRIORITIES (const int)**: Number of speech priority levels

## Dependencies
- **wpaudio/attributes.h**: Audio attribute definitions
- **wsys/File.h**: File I/O operations
- **Common/GameAudio.h**: Audio event and priority definitions
- **Common/GameSpeech.h**: Speech interface declarations
- **Common/INI.h**: Configuration file handling
- **TheAudio**: Global audio system interface
