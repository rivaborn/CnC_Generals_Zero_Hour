# GeneralsMD/Code/GameEngine/Include/Common/StatsCollector.h - Enhanced Analysis

## Architectural Role
This header defines the `StatsCollector` singleton, which serves as the engine's telemetry system for gameplay analytics. It bridges the game logic layer (command processing) with the filesystem for persistent logging, enabling post-game analysis of player behavior and performance metrics.

## Cross-References
### Incoming
- Likely called by the **GameLoop** (for `update()`), **CommandSystem** (for message stats), and **UnitManager** (for unit counts).
- May be referenced in **DebugBuilds** or **QA tools** for runtime statistics.

### Outgoing
- Interacts with **FileSystem** (via `AsciiString` and file operations).
- Depends on **GameMessage** system for command tracking.
- Uses **Timer/FrameCounter** for scroll time measurement.

## Design Patterns
- **Singleton**: Global access via `TheStatsCollector` for centralized stats collection.
- **Observer**: Passively collects data from game events (messages, unit counts).
- **Data Logger**: Accumulates metrics and periodically flushes to disk.

*Not inferable*: No clear use of Factory, Strategy, or Visitor patterns.
