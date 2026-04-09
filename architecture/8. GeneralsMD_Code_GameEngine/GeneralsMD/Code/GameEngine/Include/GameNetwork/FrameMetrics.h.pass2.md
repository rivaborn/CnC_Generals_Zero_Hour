# GeneralsMD/Code/GameEngine/Include/GameNetwork/FrameMetrics.h - Enhanced Analysis

## Architectural Role
This header defines the `FrameMetrics` class, which is central to the network synchronization subsystem. It provides runtime metrics for latency, frame rate, and packet timing, enabling adaptive network compensation in multiplayer gameplay.

## Cross-References
### Incoming
- Likely called by network synchronization manager (e.g., `GameNetwork/NetworkSync.h`)
- May be referenced by game loop timing systems (e.g., `GameEngine/GameLoop.h`)

### Outgoing
- Uses basic types from `Lib/BaseType.h`
- Relies on network definitions from `GameNetwork/NetworkDefs.h`

## Design Patterns
- **Circular Buffer**: Uses modulo-indexed arrays (`m_fpsList`, `m_latencyList`) for efficient history tracking
- **Moving Average**: Computes smoothed metrics (`m_averageLatency`, `m_averageFps`) for stable network predictions
- **State Tracking**: Maintains temporal state (`m_pendingLatencies`) for async latency responses

*Not inferable: No clear Observer or Strategy patterns evident from header alone.*
