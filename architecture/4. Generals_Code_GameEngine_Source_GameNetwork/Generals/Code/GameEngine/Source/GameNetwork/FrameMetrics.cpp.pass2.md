# Generals/Code/GameEngine/Source/GameNetwork/FrameMetrics.cpp - Enhanced Analysis

## Architectural Role
This file is part of the network synchronization subsystem, providing real-time performance metrics (FPS, latency, cushion) critical for adaptive network play. It bridges the rendering subsystem (via `TheDisplay`) with network management, enabling dynamic adjustment to connection quality.

## Cross-References
### Incoming
- Likely called by `ConnectionManager` (for latency processing) and `GameClient` (for frame updates)
- `TheDisplay` uses its metrics for HUD display

### Outgoing
- Depends on `TheDisplay` for FPS data
- Uses `TheGlobalData` for configuration (history lengths)
- Interacts with network timing utilities (`timeGetTime`)

## Design Patterns
- **Moving Average**: Uses circular buffers to maintain history and compute smoothed metrics
- **Resource Management**: Manual memory handling with `NEW`/`delete` (typical for SAGE era)
- **Singleton-like Access**: Relies on global `TheGlobalData` and `TheDisplay` for state

*Not inferable*: No clear observer pattern despite metrics being "observed" by UI/network code.
