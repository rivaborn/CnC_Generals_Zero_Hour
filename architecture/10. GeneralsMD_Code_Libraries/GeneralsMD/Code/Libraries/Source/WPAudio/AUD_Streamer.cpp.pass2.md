# GeneralsMD/Code/Libraries/Source/WPAudio/AUD_Streamer.cpp - Enhanced Analysis

## Architectural Role
This file implements the core audio streaming subsystem in the SAGE engine, managing background music and long-form audio playback. It bridges the audio device layer with file I/O, handling buffering, threading, and playback state transitions.

## Cross-References
### Incoming
- **Game Logic**: Likely called from mission/level loading systems to start background music
- **UI System**: Possibly invoked during menu transitions or cutscenes
- **Audio Mixer**: May be controlled by the master audio mixer for volume/priority adjustments

### Outgoing
- **WPAudio Subsystem**: Calls `AUD_ThreadCreate`, `AudioChannelSetVolume`, etc.
- **File System**: Uses `File::seek` and `STM_AccessFileTransfer` for streaming
- **W3D Rendering**: No direct link, but timing may sync with frame updates

## Design Patterns
- **Active Object**: Uses a dedicated service thread (`service_streams`) to manage stream buffering asynchronously
- **State Pattern**: Playback states (playing/paused/stopped) are managed via bitflags in `AudioStreamerTag`
- **Double Buffering**: Implicit in the `in`/`out` access pattern for seamless playback

*Not inferable*: Exact synchronization with the game's frame timer or audio mixer priority system.
