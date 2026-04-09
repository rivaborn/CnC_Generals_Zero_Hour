# GeneralsMD/Code/GameEngine/Include/Common/PerfTimer.h

## Purpose
Header for performance timing utilities in the SAGE engine, supporting profiling and metrics collection.

## Responsibilities
- Defines `PerfGather` and `PerfTimer` classes for performance measurement
- Provides macros for declaring and using performance timers
- Manages high-resolution timing via `QueryPerformanceCounter` or RDTSC
- Integrates with debug display and metrics systems

## Key Types
- **PerfGather (Class)**: Tracks execution time and call counts for code segments
- **PerfTimer (Class)**: Measures time over specific frame ranges with optional crash reporting
- **AutoPerfGather (Class)**: RAII wrapper for `PerfGather` timing
- **AutoPerfGatherIgnore (Class)**: RAII wrapper that ignores timer results
- **DebugDisplayInterface (Class)**: Interface for debug display (forward declared)

## Key Functions
### `GetPrecisionTimer(Int64* t)`
- Purpose: Retrieves current high-resolution timer value
- Calls: `QueryPerformanceCounter` (if `USE_QPF`) or inline assembly (`RDTSC`)

### `PerfGather::startTimer()`
- Purpose: Starts a performance measurement
- Calls: `GetPrecisionTimer`

### `PerfGather::stopTimer()`
- Purpose: Stops a performance measurement and updates metrics
- Calls: `GetPrecisionTimer`

### `PerfTimer::startTimer()`
- Purpose: Begins timing if within specified frame range
- Calls: `GetPrecisionTimer`

### `PerfTimer::stopTimer()`
- Purpose: Ends timing and optionally outputs metrics
- Calls: `GetPrecisionTimer`, `showMetrics()`, `outputInfo()`

## Globals
- **s_stopStartOverhead (Int64)**: Measures overhead of stop/start timer operations
- **m_active (PerfGather*)**: Stack of active timers
- **m_activeHead (PerfGather**)**: Pointer to current active timer
- **s_ignoring (Bool)**: Flag for ignoring timer results

## Dependencies
- `Common/GameCommon.h` (for `DUMP_PERF_STATS`)
- `GameLogic/GameLogic.h` (for `TheGameLogic`)
- `Common/PerfMetrics.h`
- `Common/GlobalData.h` (for `TheGlobalData`)
- Windows API (`QueryPerformanceCounter`) when `USE_QPF` is defined
