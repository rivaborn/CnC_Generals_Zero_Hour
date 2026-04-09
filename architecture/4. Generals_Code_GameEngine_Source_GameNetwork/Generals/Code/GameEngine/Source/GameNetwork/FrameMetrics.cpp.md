# Generals/Code/GameEngine/Source/GameNetwork/FrameMetrics.cpp

## Purpose
Manages frame rate, latency, and network cushion metrics for performance monitoring and network synchronization.

## Responsibilities
- Tracks FPS and latency history
- Calculates moving averages for performance metrics
- Manages network cushion data
- Provides access to performance statistics

## Key Types
- **FrameMetrics (Class)**: Main class for frame and network metrics tracking.

## Key Functions
### `FrameMetrics()`
- Purpose: Initializes frame metrics with default values and allocates arrays.
- Calls: None.

### `init()`
- Purpose: Resets metrics to initial values.
- Calls: None.

### `doPerFrameMetrics()`
- Purpose: Updates FPS metrics once per second.
- Calls: `TheDisplay->getAverageFPS()`.

### `processLatencyResponse()`
- Purpose: Calculates and updates latency metrics from network responses.
- Calls: None.

### `addCushion()`
- Purpose: Records network cushion data and tracks minimum cushion.
- Calls: None.

## Globals
- **TheGlobalData (External)**: Provides configuration for history lengths.
- **TheDisplay (External)**: Used to fetch current FPS.

## Dependencies
- `GameNetwork/FrameMetrics.h`
- `GameClient/Display.h`
- `GameNetwork/NetworkUtil.h`
- `PreRTS.h`
