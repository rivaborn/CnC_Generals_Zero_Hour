# GeneralsMD/Code/GameEngine/Source/GameNetwork/FrameMetrics.cpp

## Purpose
Manages frame rate, latency, and network cushion metrics for the game.

## Responsibilities
- Tracks FPS and latency history
- Calculates averages for performance metrics
- Manages network cushion data
- Provides access to performance statistics

## Key Types
- FrameMetrics (Class): Main class for frame and network metrics tracking

## Key Functions
### FrameMetrics()
- Purpose: Initializes frame metrics with default values
- Calls: None

### init()
- Purpose: Resets metrics to initial values
- Calls: None

### doPerFrameMetrics()
- Purpose: Updates FPS measurements each frame
- Calls: TheDisplay->getAverageFPS()

### processLatencyResponse()
- Purpose: Processes latency response times
- Calls: None

### addCushion()
- Purpose: Updates cushion history with new value
- Calls: None

## Globals
- None

## Dependencies
- GameNetwork/FrameMetrics.h
- GameClient/Display.h
- GameNetwork/NetworkUtil.h
- PreRTS.h
- TheGlobalData (external)
- TheDisplay (external)
