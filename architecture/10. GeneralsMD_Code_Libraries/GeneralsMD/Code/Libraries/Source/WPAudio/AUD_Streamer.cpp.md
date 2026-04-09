# GeneralsMD/Code/Libraries/Source/WPAudio/AUD_Streamer.cpp

## Purpose
Manages audio streaming functionality in the game, handling playback, buffering, and stream management.

## Responsibilities
- Initialize and manage audio streamer threads
- Control audio stream playback (start/stop/pause/resume)
- Manage stream buffering and file operations
- Handle stream attributes (volume, looping, fading)
- Provide debugging and diagnostic tools

## Key Types
- **AudioStreamerTag (Class)**: Represents an audio stream with playback state, buffering, and file access.
- **AudioStreamer (Class)**: Main streamer class managing individual streams.

## Key Functions
### AudioStreamerInit
- Purpose: Initializes the streamer system and creates the service thread.
- Calls: `ListInit`, `AUD_ThreadCreate`, `AUD_ThreadSetInterval`, `AUD_ThreadSetData`

### AudioStreamerStart
- Purpose: Starts playback of an audio stream.
- Calls: `recalcBuffering`, `STM_AccessCreate`, `AudioChannelSetVolume`, `AudioChannelSetPriority`

### streamFill
- Purpose: Fills the stream buffer with audio data from the file.
- Calls: `STM_AccessFileTransfer`, `File::seek`

### service_stream
- Purpose: Services a single stream by filling its buffer.
- Calls: `streamFill`

### AudioStreamerDump
- Purpose: Outputs diagnostic information about all active streams.
- Calls: `streamDump`, `AudioServiceInfoDump`

## Globals
- **thread (AUD_Thread*)**: The service thread for managing streams.
- **streams (ListHead)**: List of active audio streams.
- **initialized (int)**: Flag indicating if the streamer system is initialized.

## Dependencies
- Key includes: `<wpaudio/Streamer.h>`, `<wpaudio/StreamBuffering.h>`, `<wpaudio/source.h>`, `<wsys/file.h>`
- External symbols: `AUD_ThreadCreate`, `STM_AccessFileTransfer`, `AudioChannelSetVolume`, `AudioFormatBytes`
