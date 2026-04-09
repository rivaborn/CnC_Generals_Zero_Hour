# GeneralsMD/Code/GameEngine/Source/Common/System/SubsystemInterface.cpp

## Purpose
Implements the subsystem management interface for the SAGE engine, handling initialization, updates, and performance tracking.

## Responsibilities
- Manages subsystem lifecycle (init, reset, shutdown)
- Tracks performance metrics for updates and draws
- Provides timing utilities for profiling
- Handles INI configuration loading for subsystems

## Key Types
- SubsystemInterface (Class): Base class for engine subsystems
- SubsystemInterfaceList (Class): Manages collection of subsystems
- SubsystemList (Type): Container for subsystem pointers

## Key Functions
### SubsystemInterface::UPDATE
- Purpose: Measures and tracks update time for performance profiling
- Calls: GetPrecisionTimerTicksPerSec, GetPrecisionTimer, update()

### SubsystemInterface::DRAW
- Purpose: Measures and tracks draw time for performance profiling
- Calls: GetPrecisionTimerTicksPerSec, GetPrecisionTimer, draw()

### SubsystemInterfaceList::initSubsystem
- Purpose: Initializes a subsystem with configuration files
- Calls: setName, init, INI::load, INI::loadDirectory

### SubsystemInterfaceList::dumpTimesForAll
- Purpose: Generates performance report for all subsystems
- Calls: getUpdateTime, getDrawTime, getName, format

## Globals
- s_msConsumed (Real): Tracks total time consumed by subsystems (performance tracking)

## Dependencies
- PreRTS.h, SubsystemInterface.h, Xfer.h
- INI class for configuration loading
- GetPrecisionTimerTicksPerSec, GetPrecisionTimer for timing
- AsciiString for string manipulation
