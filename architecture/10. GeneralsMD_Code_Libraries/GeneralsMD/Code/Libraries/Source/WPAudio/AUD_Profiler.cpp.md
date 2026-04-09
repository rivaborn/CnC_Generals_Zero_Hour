# GeneralsMD/Code/Libraries/Source/WPAudio/AUD_Profiler.cpp

## Purpose
Audio profiling utilities for performance monitoring in the SAGE engine.

## Responsibilities
- Tracks audio cache performance metrics (hits, misses, bandwidth)
- Measures CPU usage for audio processing
- Provides profiling text output for debugging
- Manages timing intervals for profiling updates

## Key Types
- ProfileData (struct): Audio cache profiling statistics
- ProfileCPU (struct): CPU usage profiling data
- ProfStamp (typedef): Timestamp type for performance measurements

## Key Functions
### ProfCacheInit
- Purpose: Initializes audio cache profiling data
- Calls: memset, QueryPerformanceFrequency

### ProfCacheNewFrame
- Purpose: Updates frame-based profiling statistics
- Calls: None

### ProfCacheLoadStart/End
- Purpose: Tracks timing for audio data loading operations
- Calls: QueryPerformanceCounter

### ProfileCPUStart/End
- Purpose: Manages CPU profiling session lifecycle
- Calls: QueryPerformanceCounter, calc_ticks

### ProfileCPUPrint
- Purpose: Outputs formatted CPU usage statistics
- Calls: sprintf

### calc_ticks
- Purpose: Calculates elapsed time between timestamps
- Calls: None

## Globals
- None

## Dependencies
- windows.h: QueryPerformanceCounter, QueryPerformanceFrequency
- wpaudio/profiler.h: ProfileData, ProfileCPU definitions
- AudioGetTime(): External time function
