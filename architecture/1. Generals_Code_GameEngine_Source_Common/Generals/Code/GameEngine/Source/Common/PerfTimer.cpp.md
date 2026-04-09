# Generals/Code/GameEngine/Source/Common/PerfTimer.cpp

## Purpose
This file implements performance timing and metrics gathering for the game engine, including initialization of precision timers, management of performance data, and outputting performance statistics.

## Responsibilities
- Initialize and manage high-resolution timers.
- Collect and store performance metrics for different parts of the game.
- Output performance data to files or debug displays.
- Handle performance-related debugging and logging.

## Key Types
- `PerfMetricsOutput`: Manages string pairs for storing performance stats.
- `PerfGather`: Represents a performance metric gathering object with methods to start, stop, and reset timers.
- `PerfTimer`: A class for timing specific sections of code and outputting their performance metrics.

## Key Functions
### GetPrecisionTimerTicksPerSec
- Purpose: Retrieves the ticks per second of the precision timer.
- Calls: None

### InitPrecisionTimer
- Purpose: Initializes the precision timer frequency and conversion factors.
- Calls: `QueryPerformanceFrequency`, `timeGetTime`, `GetPrecisionTimer`

### PerfGather::resetAll
- Purpose: Resets all performance gatherers to their initial state.
- Calls: `PerfGather::reset`

### PerfGather::initPerfDump
- Purpose: Initializes the performance dump by opening a file and calculating overhead.
- Calls: `strcpy`, `fopen`, `GetPrecisionTimer`

### PerfGather::dumpAll
- Purpose: Dumps all performance data to a file, skipping initial frames.
- Calls: `fprintf`, `fflush`, `fclose`

### PerfTimer::outputInfo
- Purpose: Outputs performance information for a timer, either crashing or logging based on configuration.
- Calls: `DEBUG_CRASH`, `DEBUG_LOG`

## Globals
- `s_ticksPerSec (Int64)`: Stores the ticks per second of the precision timer.
- `s_ticksPerMSec (double)`: Conversion factor from ticks to milliseconds.
- `s_ticksPerUSec (double)`: Conversion factor from ticks to microseconds.
- `s_output (PerfMetricsOutput)`: Manages performance output strings.
- `s_perfStatsFile (FILE*)`: File pointer for writing performance data.

## Dependencies
- Includes: "PreRTS.h", "Common/PerfTimer.h", "Common/GlobalData.h", "GameClient/DebugDisplay.h", "GameClient/Display.h", "GameClient/GraphDraw.h"
- External symbols: `QueryPerformanceFrequency`, `timeGetTime`, `DEBUG_CRASH`, `DEBUG_LOG`, `TheGraphDraw`, `TheGlobalData`, `TheGameLogic`
