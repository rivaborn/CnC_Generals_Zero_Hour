# GeneralsMD/Code/GameEngine/Include/GameNetwork/FrameMetrics.h

## Purpose
Manages frame-based performance metrics for networked gameplay, tracking latency, FPS, and packet arrival timing.

## Responsibilities
- Tracks frame rate history over 60 seconds
- Measures round-trip latency to packet router
- Calculates average latency and FPS
- Manages packet arrival cushion metrics
- Provides metrics for network synchronization

## Key Types
- FrameMetrics (Class): Tracks game performance metrics for network synchronization

## Key Functions
### FrameMetrics()
- Purpose: Default constructor
- Calls: Not inferable

### init()
- Purpose: Initializes metrics tracking structures
- Calls: Not inferable

### reset()
- Purpose: Resets all tracking metrics
- Calls: Not inferable

### doPerFrameMetrics(UnsignedInt frame)
- Purpose: Updates per-frame metrics
- Calls: Not inferable

### processLatencyResponse(UnsignedInt frame)
- Purpose: Processes received latency responses
- Calls: Not inferable

### addCushion(Int cushion)
- Purpose: Adds packet arrival cushion data
- Calls: Not inferable

### getAverageLatency()
- Purpose: Returns average network latency
- Calls: Not inferable

### getAverageFPS()
- Purpose: Returns average frames per second
- Calls: Not inferable

### getMinimumCushion()
- Purpose: Returns minimum packet arrival cushion
- Calls: Not inferable

## Globals
- None

## Dependencies
- Lib/BaseType.h (for basic types)
- GameNetwork/NetworkDefs.h (for network definitions)
