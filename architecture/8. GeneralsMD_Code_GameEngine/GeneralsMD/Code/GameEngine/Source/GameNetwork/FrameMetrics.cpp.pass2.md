# GeneralsMD/Code/GameEngine/Source/GameNetwork/FrameMetrics.cpp - Enhanced Analysis

## Architectural Role
This file implements the `FrameMetrics` class, which is part of the network subsystem responsible for tracking and calculating performance metrics like FPS, latency, and network cushion. It serves as a central data store for network-related statistics used by other subsystems for adaptive behavior and debugging.

## Cross-References
### Incoming
- Network-related components (e.g., `ConnectionManager`) likely call `processLatencyResponse()` to update latency metrics.
- Game loop or timing system calls `doPerFrameMetrics()` to track FPS.
- UI or HUD systems may query `getAverageFPS()` and `getAverageLatency()` for display.

### Outgoing
- Depends on `TheDisplay` for FPS data (`getAverageFPS()`).
- Uses `TheGlobalData` for configuration (history lengths).
- No direct calls to other subsystems; focuses on internal state management.

## Design Patterns
- **Circular Buffer**: Uses modulo indexing (`m_fpsListIndex`, `m_cushionIndex`) to manage fixed-size history arrays efficiently.
- **Moving Average**: Implements exponential smoothing for FPS and latency calculations to reduce noise in metrics.
- **Singleton-like Access**: Relies on global `TheGlobalData` and `TheDisplay` for external state, suggesting tight coupling with engine globals.
