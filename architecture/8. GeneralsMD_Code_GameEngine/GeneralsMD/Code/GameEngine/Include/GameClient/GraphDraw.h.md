# GeneralsMD/Code/GameEngine/Include/GameClient/GraphDraw.h

## Purpose
Header for a class that queues and renders performance graphs for debugging/timing purposes.

## Responsibilities
- Manages a list of graph entries (label + value pairs)
- Renders the graph each frame
- Clears the graph when needed
- Provides global access via `TheGraphDraw`

## Key Types
- `GraphDraw` (Class): Manages graph rendering for performance timers
- `PairAsciiStringReal` (Typedef): Pair of label (string) and value (float)
- `VecGraphEntries` (Typedef): Vector of graph entries
- `DisplayString` (Class): Used for rendering text (external)

## Key Functions
### `addEntry`
- Purpose: Adds a new entry to the graph
- Calls: None visible

### `render`
- Purpose: Renders the graph during the frame
- Calls: None visible

### `clear`
- Purpose: Clears all entries from the graph
- Calls: None visible

## Globals
- `TheGraphDraw` (GraphDraw*): Global instance for graph rendering

## Dependencies
- `Common/PerfTimer.h` (PerfTimer)
- `Common/STLTypedefs.h` (STL containers)
- `DisplayString` (from UI system)
