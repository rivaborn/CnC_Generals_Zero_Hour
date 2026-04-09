# GeneralsMD/Code/Libraries/Source/WPAudio/AUD_Windows.cpp

## Purpose
Implements Windows-specific audio thread management and WAVE file parsing for the WPAudio library.

## Responsibilities
- Manages audio threads with priority control
- Handles thread synchronization via critical sections
- Parses WAVE/MP3 audio files into format structures
- Provides Windows-specific audio utilities (debug output, window handle management)

## Key Types
- `_aud_thread` (Class): Audio thread control structure with state, priority, and synchronization
- `AudioFormat` (Struct): Audio format descriptor (external)
- `AudioServiceInfo` (Struct): Audio service timing info (external)
- `ProfileCPU` (Struct): CPU profiling data (external)

## Key Functions
### `AUD_ThreadCreate`
- Purpose: Creates and starts a new audio thread with specified priority
- Calls: `CreateThread`, `SetThreadPriority`, `InitializeCriticalSection`

### `AUD_ThreadDestroy`
- Purpose: Stops and cleans up an audio thread
- Calls: `WaitForSingleObject`, `CloseHandle`, `DeleteCriticalSection`

### `AudioFormatReadWaveFile`
- Purpose: Parses WAVE/MP3 files into audio format structures
- Calls: `AudioFormatReadMP3File`, `AudioFormatUpdate`

### `WindowsDebugPrint`
- Purpose: Outputs debug strings via Windows OutputDebugString
- Calls: `OutputDebugStringA`

## Globals
- `audioMainWindowHandle` (HWND): Stores the main application window handle
- `AUD_Thread` (static): Thread management singleton instance

## Dependencies
- Windows API: `windows.h`, `mmreg.h`
- WPAudio: `thread.h`, `memory.h`, `Source.h`, `device.h`, `profiler.h`, `win32.h`
- WSys: `File.h`
