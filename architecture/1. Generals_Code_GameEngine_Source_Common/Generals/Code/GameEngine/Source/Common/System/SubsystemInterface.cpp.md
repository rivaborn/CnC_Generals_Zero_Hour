# Generals/Code/GameEngine/Source/Common/System/SubsystemInterface.cpp

## Purpose
This file implements the `SubsystemInterface` class and its associated list management, providing a framework for managing game subsystems with optional performance tracking.

## Responsibilities
- Manages initialization, update, draw, reset, and shutdown of game subsystems.
- Optionally tracks performance statistics for each subsystem's update and draw methods.

## Key Types
- **SubsystemInterface (Class)**: Represents a generic game subsystem with methods for initialization, updating, drawing, resetting, and shutting down. It also includes optional performance tracking fields.
- **SubsystemInterfaceList (Class)**: Manages a list of `SubsystemInterface` instances, providing methods to add, remove, initialize, post-process load, reset, and shut down all subsystems.

## Key Functions
### SubsystemInterface::UPDATE
- Purpose: Updates the subsystem and tracks performance if enabled.
- Calls:
  - `update()`
  - `GetPrecisionTimerTicksPerSec()`
  - `GetPrecisionTimer()`

### SubsystemInterface::DRAW
- Purpose: Draws the subsystem and tracks performance if enabled.
- Calls:
  - `draw()`
  - `GetPrecisionTimerTicksPerSec()`
  - `GetPrecisionTimer()`

### SubsystemInterfaceList::initSubsystem
- Purpose: Initializes a subsystem with configuration files and adds it to the list.
- Calls:
  - `setName()`
  - `init()`
  - `INI::load()`
  - `INI::loadDirectory()`

### SubsystemInterfaceList::shutdownAll
- Purpose: Shuts down all subsystems in reverse order and clears the list.
- Calls:
  - `delete` (for each subsystem)

## Globals
- **s_msConsumed (Real)**: Tracks total consumed time for performance statistics.

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/SubsystemInterface.h"
  - "Common/Xfer.h"
  - "GameLogic\GameLogic.h" (if `DUMP_PERF_STATS` is defined)
  - "Common/PerfTimer.h" (if `DUMP_PERF_STATS` is defined)

- External symbols used:
  - `TheSubsystemList`
  - `DEBUG_ASSERTCRASH`
  - `DEBUG_LOG`
  - `GetPrecisionTimerTicksPerSec`
  - `GetPrecisionTimer`
