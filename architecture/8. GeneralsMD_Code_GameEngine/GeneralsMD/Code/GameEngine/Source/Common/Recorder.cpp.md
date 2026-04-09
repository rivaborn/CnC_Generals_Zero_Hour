# GeneralsMD/Code/GameEngine/Source/Common/Recorder.cpp

## Purpose
Handles recording and playback of game sessions, including CRC validation and replay file management.

## Responsibilities
- Records game messages and player actions to replay files
- Manages replay file creation, naming, and storage
- Handles playback of recorded games
- Logs game start/end times, disconnections, and CRC mismatches
- Provides replay controls and UI integration

## Key Types
- **RecorderClass (Class)**: Main recorder implementation handling recording/playback
- **CRCInfo (Class)**: Tracks CRC validation state and player information
- **GameMessage (External)**: Game command/message structure

## Key Functions
### RecorderClass::logGameStart
- Purpose: Records game start time and options
- Calls: `fseek`, `fwrite`, `time`, `TheGlobalData->m_saveStats` checks

### RecorderClass::logCRCMismatch
- Purpose: Logs CRC validation failures
- Calls: `fseek`, `fwrite`, `DEBUG_LOG`

### RecorderClass::appendNextCommand
- Purpose: Reads next command from replay file during playback
- Calls: `fread`, `newInstance`, `TheCommandList->appendMessage`, `GameMessageParser` methods

### RecorderClass::readArgument
- Purpose: Reads argument data from replay file
- Calls: `fread`, `msg->append*Argument` methods

### createRecorder
- Purpose: Factory function to create RecorderClass instance
- Calls: `NEW RecorderClass`

## Globals
- **REPLAY_CRC_INTERVAL (Int)**: Interval for CRC checks during recording
- **replayExtention (const char*)**: File extension for replay files
- **lastReplayFileName (const char*)**: Default replay filename
- **startTime (time_t)**: Game start timestamp
- **TheRecorder (RecorderClass*)**: Global recorder instance

## Dependencies
- **Includes**: PreRTS.h, Recorder.h, FileSystem.h, playerlist.h, Player.h, GlobalData.h, GameEngine.h, GameWindow.h, GameWindowManager.h, InGameUI.h, Shell.h, GameText.h, LANAPICallbacks.h, GameMessageParser.h, PeerDefs.h, NetworkUtil.h, GameLogic.h, RandomValue.h, CRCDebug.h, Version.h
- **External**: GameMessage, GameMessageParser, TheCommandList, TheNameKeyGenerator, TheWindowManager, TheNetwork, TheGlobalData, TheGameLogic, TheLAN, TheGameSpyInfo, TheGameSpyGame, TheSkirmishGameInfo
