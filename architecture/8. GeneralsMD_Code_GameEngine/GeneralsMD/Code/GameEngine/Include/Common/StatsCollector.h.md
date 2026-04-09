# GeneralsMD/Code/GameEngine/Include/Common/StatsCollector.h

## Purpose
Header for a singleton class that collects and logs game statistics during gameplay.

## Responsibilities
- Tracks player commands (build, move, attack, scroll)
- Counts unit ownership (AI vs player)
- Measures scroll time
- Writes statistics to a file

## Key Types
- **StatsCollector (Class)**: Manages statistics collection and file output.
- **GameMessage (Class)**: Forward-declared message type used for stats collection.

## Key Functions
### `reset`
- Purpose: Resets all statistics and writes file header.
- Calls: `zeroOutStats`, `createFileName`, `writeInitialFileInfo`

### `collectMsgStats`
- Purpose: Processes game messages to update statistics.
- Calls: None (uses `GameMessage` data)

### `update`
- Purpose: Periodically updates statistics (called once per frame).
- Calls: `collectUnitCountStats`, `writeStatInfo`, `writeFileEnd`

### `writeFileEnd`
- Purpose: Finalizes the statistics file.
- Calls: None

## Globals
- **TheStatsCollector (StatsCollector\*)**: Singleton instance for global access.

## Dependencies
- `AsciiString`, `UnsignedInt`, `Bool`, `Int` (primitive types)
- `GameMessage` (forward-declared)
