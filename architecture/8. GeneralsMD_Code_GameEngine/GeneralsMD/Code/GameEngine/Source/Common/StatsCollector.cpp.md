# GeneralsMD/Code/GameEngine/Source/Common/StatsCollector.cpp

## Purpose
Collects and logs player statistics during gameplay for analysis.

## Responsibilities
- Tracks player commands (build, move, attack, scroll)
- Counts units owned by player and AI
- Logs statistics to a file at regular intervals
- Manages file creation and naming based on game session

## Key Types
- **StatsCollector (Class)**: Main class for collecting and logging statistics
- **None**: No additional structs/enums defined

## Key Functions
### `StatsCollector::reset()`
- Purpose: Initializes statistics collection and creates log file
- Calls: `createFileName()`, `writeInitialFileInfo()`, `zeroOutStats()`

### `StatsCollector::collectMsgStats()`
- Purpose: Processes game messages to count player commands
- Calls: None (directly)

### `StatsCollector::update()`
- Purpose: Updates statistics at regular intervals
- Calls: `collectUnitCountStats()`, `writeStatInfo()`, `zeroOutStats()`

### `StatsCollector::writeFileEnd()`
- Purpose: Writes final statistics and benchmark data to file
- Calls: `writeStatInfo()`

## Globals
- **TheStatsCollector (StatsCollector*)**: Singleton instance of StatsCollector
- **statsDir (char[255])**: Directory path for statistics files

## Dependencies
- `Common/StatsCollector.h`, `Common/FileSystem.h`, `Common/PlayerList.h`, `Common/Player.h`, `Common/GlobalData.h`, `Common/Money.h`, `GameLogic/Object.h`, `GameLogic/GameLogic.h`, `GameClient/MapUtil.h`, `GameNetwork/NetworkUtil.h`, `GameNetwork/LANAPICallbacks.h`
- Uses `TheGameLogic`, `ThePlayerList`, `TheGlobalData`, `TheFileSystem`, `TheNetwork`, `TheLAN`
