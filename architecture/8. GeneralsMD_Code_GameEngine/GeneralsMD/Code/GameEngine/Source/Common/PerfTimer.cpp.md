# GeneralsMD/Code/GameEngine/Source/Common/PerfTimer.cpp

## Purpose
Implements performance timing utilities for the SAGE engine, including high-resolution timers and profiling metrics.

## Responsibilities
- Provides high-precision timing via CPU cycle counting
- Manages performance profiling metrics (PerfGather)
- Handles performance timer initialization and calibration
- Outputs performance data to files and debug displays

## Key Types
- **PerfGather (Class)**: Performance measurement tracker
- **PerfTimer (Class)**: Frame-based performance timer
- **PerfMetricsOutput (Class)**: Stores performance metric strings
- **AutoPerfGatherIgnore (Class)**: Context manager for ignoring perf metrics

## Key Functions
### ProfileGetTime
- Purpose: Reads CPU timestamp counter into a 64-bit integer
- Calls: None (inline assembly)

### InitPrecisionTimer
- Purpose: Calibrates timer precision using QPC or timeGetTime
- Calls: QueryPerformanceCounter, QueryPerformanceFrequency, timeGetTime

### PerfGather::dumpAll
- Purpose: Writes performance metrics to CSV file
- Calls: fprintf, fflush

### PerfTimer::outputInfo
- Purpose: Logs or crashes with performance statistics
- Calls: DEBUG_CRASH, DEBUG_LOG

## Globals
- **s_ticksPerSec (Int64)**: Timer calibration value
- **s_ticksPerMSec (double)**: Ticks per millisecond
- **s_ticksPerUSec (double)**: Ticks per microsecond
- **s_output (PerfMetricsOutput)**: Stores metric output strings

## Dependencies
- "Common/PerfTimer.h"
- "Common/GlobalData.h"
- "GameClient/DebugDisplay.h"
- "GameClient/Display.h"
- "GameClient/GraphDraw.h"
- Windows API (QueryPerformanceCounter, timeGetTime)
