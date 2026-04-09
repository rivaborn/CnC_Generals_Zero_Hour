# GeneralsMD/Code/GameEngine/Include/Common/Recorder.h

## Purpose
Defines the replay system for recording and playing back game sessions in Command & Conquer Generals.

## Responsibilities
- Manages recording and playback of game sessions
- Handles replay file I/O and message streaming
- Tracks game state and player connections during replays
- Provides CRC validation for replay integrity

## Key Types
- **ReplayGameInfo (Class)**: Extends GameInfo to store replay-specific slot data
- **RecorderModeType (Enum)**: Defines recorder states (record, playback, none)
- **ReplayHeader (Struct)**: Contains metadata for replay files
- **RecorderClass (Class)**: Core replay system implementation
- **CRCInfo (Class)**: Forward declaration for CRC handling

## Key Functions
### createRecorder
- Purpose: Factory function to create the recorder instance
- Calls: Not inferable

### RecorderClass::playbackFile
- Purpose: Starts playback of a specified replay file
- Calls: readReplayHeader, initControls

### RecorderClass::updateRecord
- Purpose: Handles recording updates during game sessions
- Calls: writeToFile, logGameStart/End

### RecorderClass::updatePlayback
- Purpose: Processes playback updates frame-by-frame
- Calls: readNextFrame, appendNextCommand

## Globals
- **TheRecorder (RecorderClass*)**: Singleton instance of the recorder

## Dependencies
- Common/MessageStream.h
- GameNetwork/GameInfo.h
- SubsystemInterface (inherited)
- GameMessage, GameMessageArgumentType (used but not defined here)
