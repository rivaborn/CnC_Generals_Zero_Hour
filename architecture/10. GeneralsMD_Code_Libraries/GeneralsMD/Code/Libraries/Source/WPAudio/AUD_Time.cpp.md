# GeneralsMD/Code/Libraries/Source/WPAudio/AUD_Time.cpp

## Purpose
Provides high-resolution timing functionality for audio systems, with fallback to a less precise method if hardware support is unavailable.

## Responsibilities
- Initialize the audio timer system
- Provide high-resolution time measurement
- Fallback to a failsafe time measurement method
- Track time intervals for audio synchronization

## Key Types
- `TimeStamp` (Type): Opaque timestamp value used for timing measurements
- `LARGE_INTEGER` (Windows type): Used for high-resolution counter values

## Key Functions
### `highResGetTime`
- Purpose: Returns current time using high-resolution performance counter
- Calls: `QueryPerformanceCounter`

### `failsafeGetTime`
- Purpose: Returns current time using less precise but reliable method
- Calls: `timeGetTime`

### `InitAudioTimer`
- Purpose: Initializes the timer system, selecting high-res or failsafe method
- Calls: `QueryPerformanceFrequency`

### `AudioGetTime`
- Purpose: Returns current timestamp using the initialized timer method
- Calls: `timerFunc()`

## Globals
- `lastTime` (TimeStamp): Stores the last recorded timestamp
- `interval` (TimeStamp): Stores the time interval between measurements
- `timeOut` (TimeStamp): Stores timeout value for timing operations
- `timerFunc` (TimeStamp (*)(void)): Function pointer to active timer function
- `timerMilliSecScale` (LONGLONG): Scaling factor for converting high-res ticks to milliseconds

## Dependencies
- Windows API: `QueryPerformanceCounter`, `QueryPerformanceFrequency`, `timeGetTime`
- WPAudio headers: `wpaudio/time.h`
- Standard C: `stdio.h`, `windows.h`, `mmsystem.h`, `assert.h`
