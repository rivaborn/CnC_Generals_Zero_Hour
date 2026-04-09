# GeneralsMD/Code/Libraries/Source/profile/profile.cpp

## Purpose
This file implements the profiling system for the game, including memory management, timing, and frame tracking.

## Responsibilities
- Memory allocation/deallocation with profiling
- CPU clock cycle measurement
- Frame range tracking and recording
- Profiling result output management

## Key Types
- `ProfileCmdInterface` (Class): Command interface for profiling
- `Profile::FrameName` (Struct): Stores frame name and recording state
- `Profile::PatternListEntry` (Struct): Pattern matching for frame recording

## Key Functions
### `ProfileAllocMemory`
- Purpose: Allocates memory with profiling
- Calls: `GlobalAlloc`, `DCRASH_RELEASE`

### `ProfileReAllocMemory`
- Purpose: Reallocates memory with profiling
- Calls: `GlobalReAlloc`, `GlobalAlloc`, `GlobalFree`, `memcpy`

### `GetClockCyclesFast`
- Purpose: Measures CPU clock cycles per second
- Calls: `timeGetTime`, `QueryPerformanceCounter`, `QueryPerformanceFrequency`, `ProfileGetTime`

### `Profile::StartRange`
- Purpose: Starts recording a frame range
- Calls: `ProfileReAllocMemory`, `ProfileAllocMemory`, `SimpleMatch`, `ProfileFuncLevelTracer::FrameStart`, `ProfileId::FrameStart`

### `Profile::StopRange`
- Purpose: Stops recording a frame range
- Calls: `ProfileReAllocMemory`, `ProfileAllocMemory`, `ProfileFuncLevelTracer::FrameEnd`, `ProfileId::FrameEnd`

### `ProfileShutdown`
- Purpose: Cleans up profiling resources
- Calls: `ProfileFuncLevelTracer::Shutdown`, `ProfileId::Shutdown`, `cmd.RunResultFunctions`

## Globals
- `cmd` (ProfileCmdInterface&): Global command interface instance
- `__RegisterDebugCmdGroup_Profile` (bool): Debug command registration
- `profileTracerInit` (int): Atexit registration for shutdown

## Dependencies
- `_pch.h`, `mmsystem.h`
- `ProfileFuncLevelTracer`, `ProfileId`, `ProfileResultInterface`, `Debug`
