# GeneralsMD/Code/GameEngine/Source/Common/PerfTimer.cpp - Enhanced Analysis

## Architectural Role
This file implements the engine's performance profiling infrastructure, providing low-level timing primitives and high-level profiling metrics. It bridges the gap between hardware timing (CPU cycles/QPC) and game-specific performance analysis (frame timing, call counts).

## Cross-References
### Incoming
- **GameClient/DebugDisplay.h**: Uses `DebugDisplayInterface` for metrics display
- **GameClient/GraphDraw.h**: Integrates with `TheGraphDraw` for visual profiling
- **Common/GlobalData.h**: Checks `TheGlobalData->m_showMetrics` for display control

### Outgoing
- **Windows API**: Directly calls `QueryPerformanceCounter`, `timeGetTime` for timing
- **GameLogic**: Accesses `TheGameLogic->getFrame()` for frame-based metrics
- **File I/O**: Writes CSV dumps via `fprintf`, `fclose`

## Design Patterns
- **Singleton-like Global State**: Uses static globals (`s_ticksPerSec`, `s_output`) for engine-wide timing calibration
- **Context Manager**: `AutoPerfGatherIgnore` implements RAII for temporary metric suppression
- **Strategy Pattern**: `PerfGather::dumpAll` conditionally outputs different metrics based on `s_perfDumpOptions` flags

*Not inferable*: Exact relationship with `PerfMetricsOutput` storage mechanism.
