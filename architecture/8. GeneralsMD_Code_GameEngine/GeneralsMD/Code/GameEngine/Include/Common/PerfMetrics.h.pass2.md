# GeneralsMD/Code/GameEngine/Include/Common/PerfMetrics.h - Enhanced Analysis

## Architectural Role
This header defines timing constants used by the engine's performance measurement system, bridging the gap between the main loop and profiling tools. It enables frame-based profiling hooks for load and logic phases, critical for optimizing the SAGE engine's real-time performance.

## Cross-References
### Incoming
- Likely referenced by profiling/debug systems (e.g., `Profiler.cpp`) and main loop components (`Engine.cpp`)

### Outgoing
- None (header-only, no dependencies)

## Design Patterns
- **Constant Interface**: Exposes timing constants via enums for frame-based profiling
- **Magic Numbers**: Uses named enums to document frame boundaries (e.g., `PERFMETRICS_LOGIC_STOPFRAME = 1000`)
- **Not inferable**: No OOP patterns visible in this minimal header

*Cross-cutting insight*: These constants suggest the engine uses frame-based profiling where metrics are sampled at specific frame intervals (e.g., every 150 frames for display). The `LOGIC_STOPFRAME = 1000` hints at a 1000-frame buffer for logic timing data.
