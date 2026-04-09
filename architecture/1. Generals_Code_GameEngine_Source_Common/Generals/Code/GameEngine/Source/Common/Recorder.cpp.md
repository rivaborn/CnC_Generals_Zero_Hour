# Generals/Code/GameEngine/Source/Common/Recorder.cpp

## Purpose
This file implements the `RecorderClass`, which handles recording and playing back game sessions in Command & Conquer Generals. It manages logging game events, player actions, and CRC mismatches to replay files.

## Responsibilities
- Record game start, end, and various game events.
- Handle player disconnects and CRC mismatches during gameplay.
- Manage replay file creation and naming.
- Provide functionality to read and append commands from replay files for playback.

## Key Types
- **CRCInfo (Class)**: Manages CRC-related information for the recorder.

## Key Functions
### createRecorder
- Purpose: Creates a new instance of `RecorderClass`.
- Calls: None

### RecorderClass::logGameStart
- Purpose: Logs the start time and options of the game to the replay file.
- Calls: `fseek`, `fwrite`

### RecorderClass::logPlayerDisconnect
- Purpose: Logs player disconnection events to the replay file.
- Calls: `fseek`, `fwrite`

### RecorderClass::logCRCMismatch
- Purpose: Logs CRC mismatch events to the replay file.
- Calls: `fseek`, `fwrite`

### RecorderClass::logGameEnd
- Purpose: Logs the end time and duration of the game to the replay file.
- Calls: `fseek`, `fwrite`

## Globals
- **REPLAY_CRC_INTERVAL (Int)**: Interval for CRC checks.
- **replayExtention (const char \*)**: File extension for replay files.
- **lastReplayFileName (const char \*)**: Default name for the last replay file.
- **startTime (time_t)**: Start time of the game.
- **startTimeOffset, endTimeOffset, framesOffset, desyncOffset, quitEarlyOffset, disconOffset (UnsignedInt)**: Offsets for various data in the replay file.
- **TheRecorder (RecorderClass \*)**: Global instance of the recorder.

## Dependencies
- Key includes:
  - "Common/Recorder.h"
  - "Common/FileSystem.h"
  - "Common/playerlist.h"
  - "GameNetwork/LANAPICallbacks.h"
  - "GameLogic/GameLogic.h"
  - "Common/CRCDebug.h"
  - "Common/Version.h"
