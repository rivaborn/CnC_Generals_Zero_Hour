# GeneralsMD/Code/GameEngine/Include/Common/PerfTimer.h - Enhanced Analysis

## Architectural Role
This header provides the core performance instrumentation framework for the SAGE engine, enabling profiling across game subsystems. It bridges the timing infrastructure with debug displays and metrics systems, supporting both real-time and post-mortem analysis.

## Cross-References
### Incoming
- **GameLogic**: Uses `TheGameLogic->getFrame()` for frame-based timing
- **GlobalData**: References `TheGlobalData->m_showMetrics` for metrics display control
- **DebugDisplayInterface**: Used for metrics visualization (forward declared)

### Outgoing
- **Windows API**: Directly calls `QueryPerformanceCounter` when `USE_QPF` is enabled
- **Inline Assembly**: Uses `RDTSC` for high-resolution timing when QPF is disabled
- **PerfMetrics**: Integrates with metrics collection system (header inclusion)

## Design Patterns
- **RAII (Resource Acquisition Is Initialization)**: `AutoPerfGather` and `AutoPerfGatherIgnore` ensure timers are properly started/stopped
- **Singleton-like Global State**: Uses static members (`m_active`, `m_activeHead`) for timer stack management
- **Macro-based API**: Provides `DECLARE_PERF_TIMER`/`USE_PERF_TIMER` for lightweight instrumentation

**Note**: The `NO_PERF_TIMERS` define in debug builds suggests intentional performance optimization trade-offs.
